Software de control 	https://makecode.microbit.org/S65503-27477-55251-60335
====
huskylens.init_i2c()
huskylens.init_mode(protocolAlgorithm.ALGORITHM_COLOR_RECOGNITION)
JP = 0
nezhaV2.set_combo_motor(nezhaV2.MotorPostion.M2, nezhaV2.MotorPostion.M2)
nezhaV2.reset(nezhaV2.MotorPostion.M3)
nezhaV2.combo_run(100, nezhaV2.VerticallDirection.DOWN)

def on_forever():
    global JP
    huskylens.request()
    nezhaV2.reset(nezhaV2.MotorPostion.M3)
    if huskylens.is_appear(1, HUSKYLENSResultType_t.HUSKYLENS_RESULT_BLOCK):
        basic.pause(570)
        nezhaV2.move_to_abs_angle(nezhaV2.MotorPostion.M3, nezhaV2.ServoMotionMode.CCW, -60)
        basic.pause(1530)
        JP = JP + 1
    if JP == 12:
        nezhaV2.reset(nezhaV2.MotorPostion.M3)
        basic.pause(500)
basic.forever(on_forever)

def on_forever2():
    if PlanetX_Basic.ultrasound_sensor(PlanetX_Basic.DigitalRJPin.J4,
        PlanetX_Basic.Distance_Unit_List.DISTANCE_UNIT_CM) <= 10:
        nezhaV2.move_to_abs_angle(nezhaV2.MotorPostion.M3, nezhaV2.ServoMotionMode.CCW, -50)
        basic.pause(1500)
        basic.show_leds("""
            # . . . #
            # . . . #
            . . . . .
            . . . . .
            . # # # .
            """)
    if PlanetX_Basic.ultrasound_sensor(PlanetX_Basic.DigitalRJPin.J3,
        PlanetX_Basic.Distance_Unit_List.DISTANCE_UNIT_CM) < 12:
        nezhaV2.move_to_abs_angle(nezhaV2.MotorPostion.M3, nezhaV2.ServoMotionMode.CW, 40)
        basic.pause(5000)
        basic.show_leds("""
            # . . . #
            # . . . #
            . . . . .
            . . . . .
            . # # # .
            """)
basic.forever(on_forever2)
