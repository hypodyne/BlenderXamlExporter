# Xaml-Exporter-for-Blender

## A XAML Exporter for Blender

The Blender export script was created to make it easy to get 3D models into the XAML format for use in WPF applications. The limitations is that only certain Blender items can be exported such as 3D Models, Materials, Textures and Lamps.

### Compatibility

Blender versions:

- `io_export_xaml_legacy.py` is for Blender legacy 2.7 and less.
- `ios_export_xaml.py` is for Blender 2.8 up to the latest version.

Please note, it may work for other version but they have not yet been covered.

| Blender Versions | File                     | Windows | Linux | Mac |
| :--------------- | ------------------------ | :-----: | :---: | :-: |
| Blender 2.71     | `io_export_xaml_legacy.py` |   ✅   |  ❌  | ❌ |
| Blender 2.79     | `io_export_xaml_legacy.py` |   ✅   |  ❌  | ❌ |
| Blender 4.1      | `io_export_xaml.py`    |   ✅   |  ❌  | ❌ |

### Blender 2.7 or below

#### Installing addon

You can use the Blender user preferences window to import the script into blender.
The `io_export_xaml_legacy.py` script needs to be placed in the `C:\Program Files\Blender Foundation\Blender\2.79\scripts\addons` directory, depending on your install location and Blender version.

#### Enabling Addon

- Open Blender
- Navigate to `File > User Preferences` and select `Add-ons` tab
- Filter the list by selecting the Import-Export Category.
- Scroll to the bottom of the list and check the `Import-Export: XAML format (.xaml)` list item.
- Save User Settings.

### Blender 2.8 up to the latest version

#### Installing Addon

- Within file explorer navigate to your Blender directory, the default location should be `C:\Program Files\Blender Foundation\Blender[VERSION NUMBER]`.
- Within the Blender directory, navigate to `[VERSION NUMBER]\scripts\addons`.
- Paste `io_export_xaml.py`
- Restart Blender (if you have it open).

### Enabling

- Open Blender
- Navigate to `Edit > Preferences` and select `Add-ons` tab
- Search for `xaml` and check `Import-Export: XAML format (.xaml) `
- Save User Settings.

## Export

Once installed and enabled it should be available in the `File >> Export` list.

### Export Options

These options maybe available from the “Export to XAML” pane.
Namesace

The namespace to use with the Window and code behind. The class name will be the same as the file name.

#### Container

The Window or Resource Dictionary.

#### Panel

The layout panel to be used when using a Window.

#### Viewport

You can use the standard WPF Viewport3D or the Helix Toolkit Viewport3D. The Helix Toolkit Viewport requires your project to reference Helix Toolkit (Available via nuget)

#### Convert to Y-up

Blender uses a Z-up coordinate system while XAML typically uses Y-up.
XAML Camera

A default XAML Camera or the camera defined by Blender. If no camera in scene the default XAML camera will be added.

#### XAML Lights

Use the default XAML Lights or the ones defined by Blender.

### SUPPORT

None.
