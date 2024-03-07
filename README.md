# ALSReplicated UE 4.26/4.27/5

This is a community-based effort to fully and effectively replicate Advanced Locomotion System v4 which is permanently free on the Epic Marketplace. 

# Setting Up Your Project

- Install VS 2019/2022 and Engine sources.

- Clone the repository or download the latest release.

- Move `ALSReplicated` folder into your project's `Plugins` folder

- Add the lines below into your project's `DefaultInput.ini`, below `[/Script/Engine.InputSettings]` tag:
  
  ```
  +ActionMappings=(ActionName="JumpAction",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=SpaceBar)
  +ActionMappings=(ActionName="JumpAction",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=Gamepad_FaceButton_Bottom)
  +ActionMappings=(ActionName="StanceAction",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=LeftAlt)
  +ActionMappings=(ActionName="SprintAction",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=LeftShift)
  +ActionMappings=(ActionName="StanceAction",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=Gamepad_FaceButton_Right)
  +ActionMappings=(ActionName="SprintAction",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=Gamepad_LeftThumbstick)
  +ActionMappings=(ActionName="WalkAction",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=LeftControl)
  +ActionMappings=(ActionName="WalkAction",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=Gamepad_RightShoulder)
  +ActionMappings=(ActionName="AimAction",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=RightMouseButton)
  +ActionMappings=(ActionName="AimAction",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=Gamepad_LeftTrigger)
  +ActionMappings=(ActionName="SelectRotationMode_1",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=One)
  +ActionMappings=(ActionName="SelectRotationMode_2",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=Two)
  +ActionMappings=(ActionName="SelectRotationMode_1",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=Gamepad_DPad_Left)
  +ActionMappings=(ActionName="SelectRotationMode_2",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=Gamepad_DPad_Right)
  +ActionMappings=(ActionName="CameraAction",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=C)
  +ActionMappings=(ActionName="CameraAction",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=Gamepad_RightThumbstick)
  +ActionMappings=(ActionName="RagdollAction",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=X)
  +ActionMappings=(ActionName="RagdollAction",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=Gamepad_Special_Left)
  +ActionMappings=(ActionName="CycleOverlayUp",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=MouseScrollUp)
  +ActionMappings=(ActionName="CycleOverlayDown",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=MouseScrollDown)
  +ActionMappings=(ActionName="CycleOverlayUp",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=Gamepad_DPad_Up)
  +ActionMappings=(ActionName="CycleOverlayDown",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=Gamepad_DPad_Down)
  +ActionMappings=(ActionName="OpenOverlayMenu",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=Q)
  +ActionMappings=(ActionName="OpenOverlayMenu",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=Gamepad_LeftShoulder)
  +ActionMappings=(ActionName="UseAction",bShift=False,bCtrl=False,bAlt=False,bCmd=False,Key=E)
  +AxisMappings=(AxisName="MoveForward/Backwards",Scale=1.000000,Key=W)
  +AxisMappings=(AxisName="MoveRight/Left",Scale=1.000000,Key=D)
  +AxisMappings=(AxisName="LookUp/Down",Scale=-1.000000,Key=MouseY)
  +AxisMappings=(AxisName="LookLeft/Right",Scale=1.000000,Key=MouseX)
  +AxisMappings=(AxisName="MoveForward/Backwards",Scale=-1.000000,Key=S)
  +AxisMappings=(AxisName="MoveRight/Left",Scale=-1.000000,Key=A)
  +AxisMappings=(AxisName="MoveForward/Backwards",Scale=1.000000,Key=Gamepad_LeftY)
  +AxisMappings=(AxisName="MoveRight/Left",Scale=1.000000,Key=Gamepad_LeftX)
  +AxisMappings=(AxisName="LookUp/Down",Scale=1.000000,Key=Gamepad_RightY)
  +AxisMappings=(AxisName="LookLeft/Right",Scale=1.000000,Key=Gamepad_RightX)
  ```

- Add the lines below into your `DefaultEngine.ini`, below `[/Script/Engine.CollisionProfile]` tag (Create the tag if it doesn't exist):
  
  ```
  +Profiles=(Name="ALS_Character",CollisionEnabled=QueryAndPhysics,bCanModify=True,ObjectTypeName="Pawn",CustomResponses=((Channel="Visibility",Response=ECR_Ignore),(Channel="Camera",Response=ECR_Ignore),(Channel="Climbable",Response=ECR_Ignore)),HelpMessage="Custom collision settings for the capsule in the ALS_BaseCharacter.")
  +DefaultChannelResponses=(Channel=ECC_GameTraceChannel2,DefaultResponse=ECR_Block,bTraceType=True,bStaticObject=False,Name="Climbable")
  ```

@
