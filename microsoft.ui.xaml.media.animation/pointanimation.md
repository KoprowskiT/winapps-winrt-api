---
-api-id: T:Microsoft.UI.Xaml.Media.Animation.PointAnimation
-api-type: winrt class
---

<!-- Class syntax.
public class PointAnimation : Windows.UI.Xaml.Media.Animation.Timeline, Windows.UI.Xaml.Media.Animation.IPointAnimation
-->

# Microsoft.UI.Xaml.Media.Animation.PointAnimation

## -description
Animates the value of a [Point](/uwp/api/windows.foundation.point) property between two target values using linear interpolation over a specified [Duration](timeline_duration.md).

## -xaml-syntax
```xaml
<PointAnimation .../>
```


## -remarks
Use PointAnimation to animate the property value of any dependency property that is of type [Point](/uwp/api/windows.foundation.point).

Linear interpolation for a [Point](/uwp/api/windows.foundation.point) means that **X** and **Y** values are treated as a number and the interpolation is simply a mathematical operation.

Sometimes you'll need to use indirect property targeting in order to target a sub-property of another object that's the value of a property on the target. For example, in order to animate parts of a [PathGeometry](../microsoft.ui.xaml.media/pathgeometry.md), you need to reference some of the intermediate object-property values, until the last step in the indirect property path is truly a [Point](/uwp/api/windows.foundation.point) value. For more info on indirect property targeting and other storyboarded animation concepts, see [Storyboarded animations](/windows/apps/design/motion/storyboarded-animations) or [Property-path syntax](/windows/uwp/xaml-platform/property-path-syntax).

A PointAnimation typically has at least one of the [From](pointanimation_from.md), [By](pointanimation_by.md) or [To](pointanimation_to.md) properties set, but never all three.
+ **From only:** The animation progresses from the value specified by the **From** property to the base value of the property being animated.
+ **From and To:** The animation progresses from the value specified by the **From** property to the value specified by the **To** property.
+ **From and By:** The animation progresses from the value specified by the **From** property to the value specified by the sum of the **From** and **By** properties.
+ **To only:** The animation progresses from the animated property's base value or a previous animation's output value to the value specified by the **To** property.
+ **By only:** The animation progresses from the base value of the property being animated or a previous animation's output value to the sum of that value and the value specified by the **By** property.


The [From](pointanimation_from.md), [By](pointanimation_by.md) or [To](pointanimation_to.md) properties of a PointAnimation aren't a [Point](/uwp/api/windows.foundation.point) value. Instead these are a [Nullable](/dotnet/api/system.nullable-1?view=dotnet-uwp-10.0&preserve-view=true) for [Point](/uwp/api/windows.foundation.point). The default value for these is **null**, not an uninitialized structure. That **null** value is how the animation system distinguishes that you haven't specifically set a value. Visual C++ component extensions (C++/CX) doesn't have a [Nullable](/dotnet/api/system.nullable-1?view=dotnet-uwp-10.0&preserve-view=true) type, so it uses [IReference](/uwp/api/windows.foundation.ireference-1) instead.

## -examples
The following example shows how to use the PointAnimation to animate the [Center](../microsoft.ui.xaml.media/ellipsegeometry_center.md) property of an [EllipseGeometry](../microsoft.ui.xaml.media/ellipsegeometry.md).



[!code-cpp[Pointanimation](../microsoft.ui.xaml/code/pointanimation/cpp/Page.xaml.cpp#SnippetPointanimation_cs)]

[!code-xaml[Pointanimation](../microsoft.ui.xaml/code/pointanimation/csharp/Page.xaml#SnippetPointanimation)]


[!code-csharp[Pointanimation_cs](../microsoft.ui.xaml/code/pointanimation/csharp/Page.xaml.cs#SnippetPointanimation_cs)]

[!code-vb[Pointanimation_cs](../microsoft.ui.xaml/code/pointanimation/vbnet/Page.xaml.vb#SnippetPointanimation_cs)]

## -see-also
[Storyboarded animations](/windows/apps/design/motion/storyboarded-animations), [XAML animation sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/XAML%20animation%20library%20sample), [Timeline](timeline.md), [Point](/uwp/api/windows.foundation.point), [PointAnimationUsingKeyFrames](pointanimationusingkeyframes.md), [PointAnimationUsingKeyFrames](pointanimationusingkeyframes.md)
