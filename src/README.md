Software de control
====
(https://makecode.microbit.org/S07276-56351-08161-22981)
lamine = -250

def on_forever():
    global lamine
    nezhaV2.set_combo_motor(nezhaV2.MotorPostion.M1, nezhaV2.MotorPostion.M1)
    nezhaV2.reset(nezhaV2.MotorPostion.M2)
    basic.pause(1000)
    nezhaV2.start(nezhaV2.MotorPostion.M3, lamine)
    basic.pause(2000)
    # PRIMER SECTOR PRIMERA VUELTA
    nezhaV2.move_to_abs_angle(nezhaV2.MotorPostion.M2, nezhaV2.ServoMotionMode.CCW, -38)
    basic.pause(3270)
    nezhaV2.move_to_abs_angle(nezhaV2.MotorPostion.M2,
        nezhaV2.ServoMotionMode.SHORT_PATH,
        0)
    basic.pause(4370)
    # SEGUNDO SECTOR PRIMERA VUELTA
    nezhaV2.move_to_abs_angle(nezhaV2.MotorPostion.M2, nezhaV2.ServoMotionMode.CCW, -38)
    basic.pause(3185)
    nezhaV2.move_to_abs_angle(nezhaV2.MotorPostion.M2,
        nezhaV2.ServoMotionMode.SHORT_PATH,
        0)
    basic.pause(4350)
    # TERCER SECTOR PRIMERA VUELTA
    nezhaV2.move_to_abs_angle(nezhaV2.MotorPostion.M2, nezhaV2.ServoMotionMode.CCW, -38)
    basic.pause(3185)
    nezhaV2.move_to_abs_angle(nezhaV2.MotorPostion.M2,
        nezhaV2.ServoMotionMode.SHORT_PATH,
        0)
    basic.pause(4350)
    # CUARTO SECTOR PRIMERA VUELTA
    nezhaV2.move_to_abs_angle(nezhaV2.MotorPostion.M2, nezhaV2.ServoMotionMode.CCW, -38)
    basic.pause(3250)
    nezhaV2.move_to_abs_angle(nezhaV2.MotorPostion.M2,
        nezhaV2.ServoMotionMode.SHORT_PATH,
        0)
    nezhaV2.start(nezhaV2.MotorPostion.M3, lamine)
    basic.pause(3000)
    nezhaV2.move_to_abs_angle(nezhaV2.MotorPostion.M2, nezhaV2.ServoMotionMode.CCW, -38)
    basic.pause(3185)
    nezhaV2.move_to_abs_angle(nezhaV2.MotorPostion.M2,
        nezhaV2.ServoMotionMode.SHORT_PATH,
        0)
    basic.pause(4350)
    nezhaV2.move_to_abs_angle(nezhaV2.MotorPostion.M2, nezhaV2.ServoMotionMode.CCW, -38)
    basic.pause(3250)
    nezhaV2.move_to_abs_angle(nezhaV2.MotorPostion.M2,
        nezhaV2.ServoMotionMode.SHORT_PATH,
        0)
    basic.pause(4350)
    nezhaV2.move_to_abs_angle(nezhaV2.MotorPostion.M2, nezhaV2.ServoMotionMode.CCW, -38)
    basic.pause(3250)
    nezhaV2.move_to_abs_angle(nezhaV2.MotorPostion.M2,
        nezhaV2.ServoMotionMode.SHORT_PATH,
        0)
    basic.pause(4350)
    nezhaV2.move_to_abs_angle(nezhaV2.MotorPostion.M2, nezhaV2.ServoMotionMode.CCW, -38)
    basic.pause(3250)
    nezhaV2.move_to_abs_angle(nezhaV2.MotorPostion.M2,
        nezhaV2.ServoMotionMode.SHORT_PATH,
        0)
    basic.pause(4350)
    lamine = 0
basic.forever(on_forever)
