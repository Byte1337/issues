# ChangeLog
This is the offical github for Depression Hacked Client changelogs

# Macro Tutorial

```java
public class Bhop extends Macro {

    public Bhop() {
        super("Bhop", ActivationType.KEY_HELD, Keyboard.KEY_SPACE);
    }

    @Override
    public void onEvent(Event event) {
        if (event instanceof MoveEvent) {
            MoveEvent moveEvent = (MoveEvent) event;
            if (!mc.getPlayer().isPlayerMoving() || mc.getPlayer().isInLiquid())
                return;
            if (mc.getPlayer().isOnGround()) {
                moveEvent.getMotion().setY(0.42F);
                mc.getPlayer().getMotion().setY(0.42F);
                moveEvent.setMovementSpeed(mc.getPlayer().getMovementSpeed() * 2);
            }
        }
    }

    @Override
    public List<Class<?>> classPool() {
        List<Class<?>> classes = new ArrayList<>();
        classes.add(MoveEvent.class);
        return classes;
    }

}
```
* Download: [Test Bhop Macro](https://depressionclient.ml/assets/macros/bhop-macro.jar)
* After that you drag the macro in the macros folder (.minecraft/Depression/macros)

# Depression 1.4 Changelog
* New Bypassing Hypixel Fly
* Added AutoBlock (working on Hypixel)
* Added KillSult Module
* Added Bypassing Hypixel NoFall
* Added Boost To Scaffold
* Added OnGround Hypixel Speed
* Changed .preset Hypixel
* Added Command Predictions
* Fixed alot of bugs
* Added Chat Bypass Module
* Added AutoDisable To Killaura And ChestStealer
* Added PlayerInfo To Killaura
* Added Mineplex Antibot
* Changed Killaura Rotations
* Added .vclip Command
* Added Only Chests Option To ChesStealer Module
* Added Option To Inventory Cleaner So It Does Not Turn Off
* Added Macros
* Added A box above the player that you are hitting with killaura
* Added FionaPort
* Added SpartanHop
* Added NoGround NoFall
* Added ThridPerson Player Model Rotation
* Added Hypixel LongJump
* Made Hypixel Fly Faster
* Fixed a clickgui bug
