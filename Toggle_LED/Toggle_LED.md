# Toggle_LED Macro
This macro allows you to control a PWM-LED connected to your printer mainboard.
To add this marco to your printer follow below steps:
1. Open up ratos.local/ in your browser.
2. Navigate to the Machine tab.
3. Open up your Printer.cfg.
4. Navigate down to the User Overrides.
5. Add the following code:
> [output_pin LED]
>
> pin: PD15       # use the pin connected to your LED
>
> pwm: True
>
> hardware_pwm: True
>
> cycle_time: 0.001
>
> shutdown_value: 0
>
> [gcode_macro Toggle_Led]
> 
> description: Toggle The LED Bar On/Off, Alternativly Set It To A Specific Intensity
> 
> variable_state: 'off'
> 
> gcode:
> 
>     {% if params.S is defined%}
>     
>     {% set S = params.S|default(0.0)|float %}
>     
>     SET_PIN PIN=LED VALUE={S}
>     
>     {%else%}
>     
>        {%if printer['output_pin LED'].value == 0 %}
>        
>           SET_PIN PIN=LED VALUE=1
>           
>        {% else %}
>        
>           SET_PIN PIN=LED VALUE=0
>           
>        {%endif%}
>        
>     {%endif%}
