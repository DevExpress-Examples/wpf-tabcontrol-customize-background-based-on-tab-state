<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/128641870/22.2.2%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/T327852)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
<!-- default badges end -->

# WPF Tab Control - Customize Tab Background for Selected, Focused, and Hovered States

This example demonstrates how to customize the background color of tabs based on their state (selected, focused, hovered).

![WPF Tab Control - Customize Tab Background for Selected, Focused, and Hovered States](https://raw.githubusercontent.com/DevExpress-Examples/how-to-change-the-tab-background-in-dxtabcontrol-when-a-tab-is-selected-focused-or-hovered-t327852/22.2.2%2B/i/wpf-tab-control-appearance-customization-devexpress.png)

The following properties are used:

* [DXTabItem.NormalBackgroundTemplate](https://documentation.devexpress.com/WPF/DevExpressXpfCoreDXTabItem_NormalBackgroundTemplatetopic.aspx)
* [DXTabItem.HoverBackgroundTemplate](https://docs.devexpress.com/WPF/DevExpress.Xpf.Core.DXTabItem.HoverBackgroundTemplate)
* [DXTabItem.SelectedBackgroundTemplate](https://documentation.devexpress.com/WPF/DevExpressXpfCoreDXTabItem_SelectedBackgroundTemplatetopic.aspx)
* [DXTabItem.FocusedBackgroundTemplate](https://documentation.devexpress.com/WPF/DevExpressXpfCoreDXTabItem_FocusedBackgroundTemplatetopic.aspx)

```xaml
<dx:DXTabControl Name="tabControl" BackgroundTemplate="{StaticResource TabControlBackground}">
    <dx:DXTabControl.ItemContainerStyle>
        <Style TargetType="dx:DXTabItem">
            <Setter Property="HoverBackgroundTemplate" Value="{StaticResource TabItemHoverBackground}"/>
            <Setter Property="NormalBackgroundTemplate" Value="{StaticResource TabItemNormalBackground}"/>
            <Setter Property="SelectedBackgroundTemplate" Value="{StaticResource TabItemSelectedBackground}"/>
            <Setter Property="FocusedBackgroundTemplate" Value="{StaticResource TabItemFocusedBackground}"/>
        </Style>
    </dx:DXTabControl.ItemContainerStyle>
    <dx:DXTabItem Header="Original Text">
        <TextBox/>
    </dx:DXTabItem>
    <dx:DXTabItem Header="Edited Text">
        <TextBox/>
    </dx:DXTabItem>
    <dx:DXTabItem Header="Result Text">
        <TextBox/>
    </dx:DXTabItem>
</dx:DXTabControl>
```

## Files to Review

* [MainWindow.xaml](./CS/DXTabControlExample/MainWindow.xaml) (VB: [MainWindow.xaml](./VB/DXTabControlExample/MainWindow.xaml))


## Documentation

* [Tab Control - Appearance Customization](https://docs.devexpress.com/WPF/113899/controls-and-libraries/layout-management/tab-control/concepts/appearance-customization)
* [DXTabControl.BackgroundTemplate](https://docs.devexpress.com/WPF/DevExpress.Xpf.Core.DXTabControl.BackgroundTemplate)
