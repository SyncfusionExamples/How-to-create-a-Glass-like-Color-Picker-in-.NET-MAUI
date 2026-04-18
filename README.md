# How to create a Glass like Color Picker in .NET MAUI

Syncfusion’s [.NET MAUI Color Picker](https://www.syncfusion.com/maui-controls/maui-colorpicker) provides built-in support for a glass-like visual effect through the [EnableLiquidGlassEffect](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Inputs.SfColorPicker.html#Syncfusion_Maui_Inputs_SfColorPicker_EnableLiquidGlassEffect) property.

To enable or disable the liquid glass effect on the ColorPicker, set the `EnableLiquidGlassEffect` property in ColorPicker:

* When `EnableLiquidGlassEffect = true`, a subtle glass-like effect is applied to every elements in the ColorPicker, enhancing its modern aesthetic.
* When `EnableLiquidGlassEffect = false`, the ColorPicker displays its default appearance.

The SfGlassEffectView can be used as a container for the Color Picker to apply a localized glass‑like visual effect, especially when the control is placed over rich backgrounds such as images.

* Wrapping the Color Picker inside [SfGlassEffectView](https://help.syncfusion.com/cr/maui/Syncfusion.Maui.Core.SfGlassEffectView.html) applies a translucent glass effect to the enclosed area.
* The `CornerRadius`, `HeightRequest`, and `WidthRequest` properties control the shape and size of the glass container.

**Additional Customizations**

The following properties are commonly used to enhance the appearance of the Color Picker when used inside a glass effect view:

* `DisplayViewStrokeThickness`
* `SliderThumbFill`
* `SliderThumbStroke`
* `PopupBackground`

> This feature is supported only on .NET 10, along with iOS 26 and macOS 26.

**MainPage.xaml**
```
<ContentPage xmlns="http://schemas.microsoft.com/dotnet/2021/maui"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             xmlns:inputs="clr-namespace:Syncfusion.Maui.Inputs;assembly=Syncfusion.Maui.Inputs"
             xmlns:core="clr-namespace:Syncfusion.Maui.Core;assembly=Syncfusion.Maui.Core"
             x:Class="ColorPicker.MainPage">

    <Grid>
        <Image Source="beach2.jpg" Aspect="AspectFill" />
        <core:SfGlassEffectView CornerRadius="16" HeightRequest="32" WidthRequest="70" VerticalOptions="Start" Margin="0, 12">
            <inputs:SfColorPicker EnableLiquidGlassEffect="True" DisplayViewStrokeThickness="0" SliderThumbFill="White" SliderThumbStroke="Transparent" PopupBackground="Transparent" />
        </core:SfGlassEffectView>
    </Grid>

</ContentPage>

```