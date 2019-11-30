# Autonomous-code_superhvarn_Skystone-2019
package org.firstinspires.ftc.teamcode;
import com.qualcomm.robotcore.hardware.DcMotor;
import com.qualcomm.robotcore.hardware.CRServo;
import com.qualcomm.robotcore.hardware.Servo;
import com.qualcomm.robotcore.util.ElapsedTime;
import com.qualcomm.robotcore.eventloop.opmode.LinearOpMode;

import org.firstinspires.ftc.robotcore.external.Telemetry;

public class autonomous extends LinearOpMode {
/*
Syborgs 10696 Autonomous Code
hardware to map:
* DcMotor - Front Left, Front Right, Rear Left, Rear Right
* DcMotor - Left Intake and Right Intake
* ARM - DcMotor Elevator, CRservo Drop Intake and Clamp
*/
   public void mapMotors () {
       frontLeftMotor = hardwareMap.get(DcMotor.class, "frontLeft");
       frontRightMotor = hardwareMap.get(DcMotor.class, "frontRight");
       rearLeftMotor = hardwareMap.get(DcMotor.class, "rearLeft");
       rearRightMotor = hardwareMap.get(DcMotor.class, "rearRight");
   }
   // declare motors for mapping
   private static DcMotor frontLeftMotor, frontRightMotor, rearLeftMotor, rearRightMotor;
   private static DcMotor LIntake, RIntake;
   private static DcMotor elevator;
   private static CRServo dropIntake, clamp;
   private static Servo LHook, RHook;
   // initialize
   public void runOpMode(int distance) throws InterruptedException {
       // map motors

       ElapsedTime runtime = new ElapsedTime();

       // run encoders for motors
       frontLeftMotor.setMode(DcMotor.RunMode.RUN_USING_ENCODER);
       frontRightMotor.setMode(DcMotor.RunMode.RUN_USING_ENCODER);
       rearLeftMotor.setMode(DcMotor.RunMode.RUN_USING_ENCODER);
       rearRightMotor.setMode(DcMotor.RunMode.RUN_USING_ENCODER);
       // reset encoders for motors
       frontLeftMotor.setMode(DcMotor.RunMode.STOP_AND_RESET_ENCODER);
       frontRightMotor.setMode(DcMotor.RunMode.STOP_AND_RESET_ENCODER);
       rearLeftMotor.setMode(DcMotor.RunMode.STOP_AND_RESET_ENCODER);
       rearRightMotor.setMode(DcMotor.RunMode.STOP_AND_RESET_ENCODER);
       // get into position
       frontLeftMotor.setMode(DcMotor.RunMode.RUN_TO_POSITION);
       frontRightMotor.setMode(DcMotor.RunMode.RUN_TO_POSITION);
       rearLeftMotor.setMode(DcMotor.RunMode.RUN_TO_POSITION);
       rearRightMotor.setMode(DcMotor.RunMode.RUN_TO_POSITION);
       // map intakes and arm
       LIntake = hardwareMap.get(DcMotor.class, "leftIntake");
       RIntake = hardwareMap.get(DcMotor.class, "rightIntake");
       elevator = hardwareMap.get(DcMotor.class, "elevator");
       dropIntake = hardwareMap.get(CRServo.class, "dropIntake");
       clamp = hardwareMap.get(CRServo.class, "clamp");
       LHook = hardwareMap.get(Servo.class, "leftHook");
       RHook = hardwareMap.get(Servo.class, "rightHook");
       double power = 0.6;
       double turn_power = -0.5;
       waitForStart();
       drive(0.6, 6);
       LHook.setPower(-1.0);
      RHook.setPower(-1);
    drive(0, 1);
    drive(-0.6, 6);
    frontLeftMotor.setPower(1);
    rearLeftMotor.setPower(1);
    frontRightMotor.setPower(-1);
    rearRightMotor.setPower(-1);
// crossing alliance bridge
    drive(0.6, 132);
     frontLeftMotor.setPower(-1);
    rearLeftMotor.setPower(-1);
    frontRightMotor.setPower(1);
    rearRightMotor.setPower(1);
   drop.setPower(1);
   clamp.setPower(1);
   frontLeftMotor.setPower(-1);
   rearLeftMotor.setPower(-1);
   frontRightMotor.setPower(1);
   rearRightMotor.setPower(1);
   drive(0.6, 132);
   clamp.setPower(-1);
   frontLeftMotor.setPower(1);
   rearLeftMotor.setPower(1);
   frontRightMotor.setPower(-1);
   rearRightMotor.setPower(-1);
   drive(0.6, 126);
   drop.setPower(-1);
   frontLeftMotor.setPower(-1);
   rearLeftMotor.setPower(-1);
   frontRightMotor.setPower(1);
   rearRightMotor.setPower(1);
   
   drop.setPower(1);
 clamp.setPower(1);
 frontLeftMotor.setPower(-1);
 rearLeftMotor.setPower(-1);
 frontRightMotor.setPower(1);
 rearRightMotor.setPower(1);
 drop.setPower(-1);
 drive(0.6, 126);
 drop.setPower(0.8);
 sleep(1000;)
 clamp.setPower(-1);
 drive(-0.6, 118);
 drop.setPower(-0.8);
 frontLeftMotor.setPower(1);
 rearLeftMotor.setPower(1);
 frontRightMotor.setPower(-1);
 rearRightMotor.setPower(-1);
 drop.setPower(1);
 sleep(1000);
 clamp.setPower(1);
 frontLeftMotor.setPower(-1);
 rearLeftMotor.setPower(-1);
 frontRightMotor.setPower(1);
 rearRightMotor.setPower(1);
 drop.setPower(-1);
 drive(0.6, 118);
 drop.setPower(0.6);
 clamp.setPower(-1);
 drive(-0.6, 110);
 frontLeftMotor.setPower(1);
 rearLeftMotor.setPower(1);
 frontRightMotor.setPower(-1);
 rearRightMotor.setPower(-1);
 drop.setPower(1);
 sleep(1000);
 clamp.setPower(1);
 sleep(1000);
 drop.setPower(-1);
 frontLeftMotor.setPower(-1);
 rearLeftMotor.setPower(-1);
 frontRightMotor.setPower(1);
 rearRightMotor.setPower(1);
 drive(0.6, 110);
 drop(0.4);
 sleep(1000);
 clamp(-1);
drive(-0.6, 102);

frontLeftMotor.setPower(1);
rearLeftMotor.setPower(1);
frontRightMotor.setPower(-1);
rearRightMotor.setPower(-1);
drop.setPower(1);
sleep(1000);
clamp.setPower(1);
sleep(1000);
drop.setPower(-1);
frontLeftMotor.setPower(-1);
rearLeftMotor.setPower(-1);
frontRightMotor.setPower(1);
rearRightMotor.setPower(1);
drive(0.6, 102);
drop(0.2);
sleep(1000);
clamp(-1)
drive(-0.6, 94);
frontLeftMotor.setPower(1);
rearLeftMotor.setPower(1);
frontRightMotor.setPower(-1);
rearRightMotor.setPower(-1);
drop.setPower(1);
sleep(1000);
clamp.setPower(1);
sleep(1000);
drop.setPower(-1);
frontLeftMotor.setPower(-1);
rearLeftMotor.setPower(-1);
frontRightMotor.setPower(1);
rearRightMotor.setPower(1);
drive(0.6, 94);
drop(0.1);
sleep(1000);
clamp(-1)
frontLeftMotor.setPower(0);
rearLeftMotor.setPower(0);
frontRightMotor.setPower(0);
rearRightMotor.setPower(0);
   public void drive (double power, double val) {
       sleep(time);
       runtime.reset();
             while (opModeIsActive()) {
           telemetry.addData("front Left Motor: ", FLposition);
           telemetry.addData("front Right Motor: ", FRposition);
           final Telemetry.Item item = telemetry.addData("rear Left Motor: ", BLposition);
           telemetry.addData("rear Right Motor", BRposition);
           telemetry.update();
           frontLeftMotor.setTargetPosition(-distance);
           frontRightMotor.setTargetPosition(distance);
           rearLeftMotor.setTargetPosition(-distance);
           rearRightMotor.setTargetPosition(distance);
           frontLeftMotor.setTargetPosition((int) + frontLeftMotor.getCurrentPosition() +  (val* AndyTICKS_PER_INCH)));
           rearLeftMotor.setTargetPosition((int) + rearLeftMotor.getCurrentPosition() +  (val* TICKS_PER_INCH)));
           frontRightMotor.setTargetPosition((int) + frontRightMotor.getCurrentPosition() +  (val*TICKS_PER_INCH)));
           rearRightMotor.setTargetPosition((int) + rearRightMotor.getCurrentPosition() +  (val*TICKS_PER_INCH)));

           frontLeftMotor.setMode(DcMotor.RunMode.RUN_TO_POSITION);
           frontRightMotor.setMode(DcMotor.RunMode.RUN_TO_POSITION);
           rearLeftMotor.setMode(DcMotor.RunMode.RUN_TO_POSITION);
           rearRightMotor.setMode(DcMotor.RunMode.RUN_TO_POSITION);
           frontLeftMotor.setPower(power);
           frontRightMotor.setPower(power);
           rearRightMotor.setPower(power);
           rearLeftMotor.setPower(power);
       while (frontLeftMotor.isBusy() && frontRightMotor.isBusy() && rearRightMotor.isBusy() && rearLeftMotor.isBusy()) {

       }


           idle();

       }
   }
}




