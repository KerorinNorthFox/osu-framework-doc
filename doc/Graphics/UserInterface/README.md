# osu.Framework.Graphics.UserInterface Doc
- [osu.Framework.Graphics.UserInterface Doc](#osuframeworkgraphicsuserinterface-doc)
- [インターフェース](#インターフェース)
  - [`IHasCurrentValue<T>` #](#ihascurrentvaluet-)
- [クラス](#クラス)
  - [`BasicButton` #](#basicbutton-)
  - [`BasicCheckbox` #](#basiccheckbox-)
  - [`BasicColourPicker` #](#basiccolourpicker-)
  - [`BasicDirectorySelector` #](#basicdirectoryselector-)
  - [`BasicDirectorySelectorBreadcrumbDisplay` #](#basicdirectoryselectorbreadcrumbdisplay-)
  - [`BasicDirectorySelectorDirectory` #](#basicdirectoryselectordirectory-)
  - [`BasicDirectorySelectorParentDirectory` #](#basicdirectoryselectorparentdirectory-)
  - [`BasicDropdown<T>` #](#basicdropdownt-)
  - [`BasicFileSelector` #](#basicfileselector-)
- [`BasicHSVColourPicker` #](#basichsvcolourpicker-)
  - [`BasicHexColourPicker` #](#basichexcolourpicker-)
  - [`BasicMenu` #](#basicmenu-)
  - [`BasicPasswordTextBox` #](#basicpasswordtextbox-)
  - [`BasicPopover` #](#basicpopover-)
  - [`BasicRearrangeableListContainer<TModel>` #](#basicrearrangeablelistcontainertmodel-)
  - [`BasicRearrangeableListItem<TModel>` #](#basicrearrangeablelistitemtmodel-)
  - [`BasicSliderBar<T>` #](#basicsliderbart-)
  - [`BasicTabControl<T>` #](#basictabcontrolt-)
  - [`BasicTextBox` #](#basictextbox-)
  - [`Button` #](#button-)
  - [`Caret` #](#caret-)
  - [`CheckBox` #](#checkbox-)
  - [`CircularBlob` #](#circularblob-)
  - [`CircularProgress` #](#circularprogress-)
  - [`CircularProgressTransformSequenceExtensions` #](#circularprogresstransformsequenceextensions-)
  - [`ColourPicker` #](#colourpicker-)
  - [`Counter` #](#counter-)
  - [`CounterTransformSequenceExtensions` #](#countertransformsequenceextensions-)
  - [`DirectorySelector` #](#directoryselector-)
  - [`DirectorySelectorBreadcrumbDisplay` #](#directoryselectorbreadcrumbdisplay-)
  - [`DirectorySelectorDirectory` #](#directoryselectordirectory-)
  - [`DirectorySelectorItem` #](#directoryselectoritem-)
  - [`Dropdown<T>` #](#dropdownt-)
  - [`DropdownHeader` #](#dropdownheader-)
  - [`DropdownMenuItem` #](#dropdownmenuitem-)
  - [`FileSelector` #](#fileselector-)
  - [`HSVColourPicker` #](#hsvcolourpicker-)
  - [`HSVColourPicker` #](#hsvcolourpicker--1)
  - [`HSVColourPicker` #](#hsvcolourpicker--2)
  - [`HexColourPicker` #](#hexcolourpicker-)
  - [`Mene` #](#mene-)
  - [`MenuItem` #](#menuitem-)
  - [`Popover` #](#popover-)
  - [`SliderBar<T>` #](#sliderbart-)
  - [`TabControl<T>` #](#tabcontrolt-)
  - [`TabItem` #](#tabitem-)
  - [`TabItem<T>` #](#tabitemt-)
  - [`TextBox` #](#textbox-)
- [列挙型](#列挙型)
  - [`MenuState` #](#menustate-)
  - [`MenuItemState` #](#menuitemstate-)

# インターフェース
## `IHasCurrentValue<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/IHasCurrentValue.cs#L12)
```csharp
public interface IHasCurrentValue<T>
```

# クラス
## `BasicButton` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/BasicButton.cs#L14)
```csharp
public partial class BasicButton : Button
```

## `BasicCheckbox` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/BasicCheckbox.cs#L16)
```csharp
public partial class BasicCheckbox : Checkbox
```

## `BasicColourPicker` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/BasicColourPicker.cs#L6)
```csharp
public partial class BasicColourPicker : ColourPicker
```

## `BasicDirectorySelector` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/BasicDirectorySelector.cs#L12)
```csharp
public partial class BasicDirectorySelector : DirectorySelector
```

## `BasicDirectorySelectorBreadcrumbDisplay` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/BasicDirectorySelectorBreadcrumbDisplay.cs#L13)
```csharp
public partial class BasicDirectorySelectorBreadcrumbDisplay : DirectorySelectorBreadcrumbDisplay
```

## `BasicDirectorySelectorDirectory` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/BasicDirectorySelectorDirectory.cs#L11)
```csharp
public partial class BasicDirectorySelectorDirectory : DirectorySelectorDirectory
```

## `BasicDirectorySelectorParentDirectory` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/BasicDirectorySelectorParentDirectory.cs#L9)
```csharp
public partial class BasicDirectorySelectorParentDirectory : BasicDirectorySelectorDirectory
```

## `BasicDropdown<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/BasicDropdown.cs#L10)
```csharp
public partial class BasicDropdown<T> : Dropdown<T>
```

## `BasicFileSelector` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/BasicFileSelector.cs#L13)
```csharp
public partial class BasicFileSelector : FileSelector
```

# `BasicHSVColourPicker` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/BasicHSVColourPicker.cs#L10)
```csharp
public partial class BasicHSVColourPicker : HSVColourPicker
```

## `BasicHexColourPicker` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/BasicHexColourPicker.cs#L8)
```csharp
public partial class BasicHexColourPicker : HexColourPicker
```

## `BasicMenu` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/BasicMenu.cs#L9)
```csharp
public partial class BasicMenu : Menu
```

## `BasicPasswordTextBox` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/BasicPasswordTextBox.cs#L8)
```csharp
public partial class BasicPasswordTextBox : BasicTextBox, ISuppressKeyEventLogging
```

## `BasicPopover` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/BasicPopover.cs#L10)
```csharp
public partial class BasicPopover : Popover
```

## `BasicRearrangeableListContainer<TModel>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/BasicRearrangeableListContainer.cs#L17)
```csharp
public partial class BasicRearrangeableListContainer<TModel> : RearrangeableListContainer<TModel>
```

## `BasicRearrangeableListItem<TModel>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/BasicRearrangeableListContainer.cs#L41)
```csharp
public partial class BasicRearrangeableListItem<TModel> : RearrangeableListItem<TModel>
```

## `BasicSliderBar<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/BasicSliderBar.cs#L11)
```csharp
public partial class BasicSliderBar<T> : SliderBar<T>
    where T : struct, IComparable<T>, IConvertible, IEquatable<T>
```

## `BasicTabControl<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/BasicTabControl.cs#L11)
```csharp
public partial class BasicTabControl<T> : TabControl<T>
```

## `BasicTextBox` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/BasicTextBox.cs#L14)
```csharp
public partial class BasicTextBox : TextBox
```

## `Button` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/Button.cs#L8)
```csharp
public abstract partial class Button : ClickableContainer
```

## `Caret` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/Caret.cs#L12)
```csharp
public abstract partial class Caret : CompositeDrawable
```

## `CheckBox` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/Checkbox.cs#L13)
```csharp
public abstract partial class Checkbox : Container, IHasCurrentValue<bool>
```

## `CircularBlob` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/CircularBlob.cs#L15)
```csharp
public partial class CircularBlob : Sprite
```

## `CircularProgress` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/CircularProgress.cs#L18)
```csharp
public partial class CircularProgress : Sprite, IHasCurrentValue<double>
```

## `CircularProgressTransformSequenceExtensions` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/CircularProgress.cs#L163)
```csharp
public static class CircularProgressTransformSequenceExtensions
```

## `ColourPicker` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/ColourPicker.cs#L13)
```csharp
public abstract partial class ColourPicker : CompositeDrawable, IHasCurrentValue<Colour4>
```

## `Counter` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/Counter.cs#L12)
```csharp
public partial class Counter : CompositeDrawable
```

## `CounterTransformSequenceExtensions` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/Counter.cs#L44)
```csharp
public static class CounterTransformSequenceExtensions
```

## `DirectorySelector` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/DirectorySelector.cs#L22)
```csharp
public abstract partial class DirectorySelector : CompositeDrawable
```

## `DirectorySelectorBreadcrumbDisplay` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/DirectorySelectorBreadcrumbDisplay.cs#L17)
```csharp
public abstract partial class DirectorySelectorBreadcrumbDisplay : CompositeDrawable
```

## `DirectorySelectorDirectory` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/DirectorySelectorDirectory.cs#L15)
```csharp
public abstract partial class DirectorySelectorDirectory : DirectorySelectorItem
```

## `DirectorySelectorItem` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/DirectorySelectorItem.cs#L13)
```csharp
public abstract partial class DirectorySelectorItem : CompositeDrawable
```

## `Dropdown<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/Dropdown.cs#L30)
```csharp
public abstract partial class Dropdown<T> : CompositeDrawable, IHasCurrentValue<T>
```

## `DropdownHeader` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/DropdownHeader.cs#L18)
```csharp
public abstract partial class DropdownHeader : ClickableContainer, IKeyBindingHandler<PlatformAction>
```

## `DropdownMenuItem` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/DropdownMenuItem.cs#L9)
```csharp
public class DropdownMenuItem<T> : MenuItem
```

## `FileSelector` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/FileSelector.cs#L20)
```csharp
public abstract partial class FileSelector : DirectorySelector
```

## `HSVColourPicker` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/HSVColourPicker.cs#L13)
```csharp
public abstract partial class HSVColourPicker : CompositeDrawable, IHasCurrentValue<Colour4>
```

## `HSVColourPicker` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/HSVColourPicker_HueSelector.cs#L18)
```csharp
public abstract partial class HueSelector : CompositeDrawable
```

## `HSVColourPicker` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/HSVColourPicker_SaturationValueSelector.cs#L20)
```csharp
public abstract partial class HSVColourPicker
```

## `HexColourPicker` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/HexColourPicker.cs#L10)
```csharp
public abstract partial class HexColourPicker : CompositeDrawable, IHasCurrentValue<Colour4>
```

## `Mene` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/Menu.cs#L24)
```csharp
public abstract partial class Menu : CompositeDrawable, IStateful<MenuState>
```

## `MenuItem` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/MenuItem.cs#L11)
```csharp
public class MenuItem
```

## `Popover` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/Popover.cs#L22)
```csharp
public abstract partial class Popover : OverlayContainer
```

## `SliderBar<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/SliderBar.cs#L14)
```csharp
public abstract partial class SliderBar<T> : Container, IHasCurrentValue<T>
    where T : struct, IComparable<T>, IConvertible, IEquatable<T>
```

## `TabControl<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/TabControl.cs#L32)
```csharp
public abstract partial class TabControl<T> : CompositeDrawable, IHasCurrentValue<T>, IKeyBindingHandler<PlatformAction>
```

## `TabItem` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/TabItem.cs#L13)
```csharp
public abstract partial class TabItem : ClickableContainer
```

## `TabItem<T>` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/TabItem.cs#L21)
```csharp
public abstract partial class TabItem<T> : TabItem
```

## `TextBox` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/TextBox.cs#L30)
```csharp
public abstract partial class TextBox : TabbableContainer, IHasCurrentValue<string>, IKeyBindingHandler<PlatformAction>
```



# 列挙型
## `MenuState` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/Menu.cs#L956)
```csharp
public enum MenuState
```

## `MenuItemState` [#](https://github.com/ppy/osu-framework/blob/master/osu.Framework/Graphics/UserInterface/Menu.cs#L962)
```csharp
public enum MenuItemState
```