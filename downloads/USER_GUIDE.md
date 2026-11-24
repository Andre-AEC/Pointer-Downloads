# Pointer by AEC Simple — User Guide

Pointer helps an audience follow your cursor during presentations and screen sharing. It draws a translucent circle around the pointer and can show a brief ripple when you left-click or right-click.

This guide and the [installer file](Pointer-by-AEC-Simple-Setup.exe) are together in the public downloads folder.

## Install and open

1. On a 64-bit Windows PC, download [Pointer by AEC Simple Setup](https://github.com/Andre-AEC/Pointer-Downloads/releases/latest/download/Pointer-by-AEC-Simple-Setup.exe) and run it. The installer is unsigned, so Windows may ask you to confirm that you want to run it.
2. Open **Pointer by AEC Simple** from the Windows Start menu.

The installer includes the .NET components Pointer needs. You do not need to install the .NET Desktop Runtime separately.

The installer also starts **Pointer Monitor** and adds it to Windows startup. Pointer Monitor appears in the system tray. Pointer's settings window appears on the taskbar and may start minimized; click its taskbar button to open it. The pointer effects are active whenever Pointer is running and their individual checkboxes are selected.

## Use Pointer

- Move the mouse to show the circle. Left-click or right-click to show a ripple.
- Press **Win+Shift+H** to open or close Pointer. You can change this shortcut in the settings window. The shortcut works while Pointer Monitor is running.
- Click **Close** in Pointer's window to exit Pointer. This does not exit Pointer Monitor.
- To open Pointer from the tray, right-click **Pointer Monitor** and choose **Open Pointer**. Double-clicking its tray icon also opens Pointer.

Opening Pointer again from the Start menu while it is already running brings its settings window forward.

## Change settings

Changes take effect immediately and save automatically. There is no Save button.

| Setting | What it does |
| --- | --- |
| **Pointer circle** | Shows or hides the circle around the cursor. |
| **Click ripples** | Shows or hides the left-click and right-click ripples. |
| **Circle diameter** | Sets the circle size from 16 to 240 pixels. Use the slider or type a number. |
| **Transparency** | Sets the effect transparency from 0% (most solid) to 90% (most see-through). Use the slider or type a number. |
| **Circle color**, **Left click color**, **Right click color** | Click a color swatch to choose a color. |
| **Toggle shortcut** | Choose a key combination to open or close Pointer. |
| **Minimize on open** | Starts the settings window minimized when you open Pointer yourself. The pointer effects still run. |
| **Auto-enable during Teams/Zoom sharing (experimental)** | Lets Pointer Monitor start Pointer when it detects sharing. This is off by default. |

Your preferences are saved for your Windows account in `%APPDATA%\MouseHighlighter\settings.json`.

## Automatic start during screen sharing

Check **Auto-enable during Teams/Zoom sharing (experimental)** in Pointer's settings window. Keep **Pointer Monitor** running in the system tray. When it detects sharing in the Windows desktop version of Teams or Zoom, it starts Pointer with the settings window minimized, regardless of **Minimize on open**.

If the monitor started Pointer, it closes Pointer about five seconds after sharing stops. If you restore Pointer's window yourself, it leaves Pointer open. If you close Pointer during a share, the monitor waits until the next share to start it again. The shortcut remains available for manual control.

Detection looks for visible sharing controls in Teams and Zoom. It can miss a share when those controls are hidden or after either meeting app changes its interface. If you share only one application window, your audience may not see Pointer's separate overlay even when you see it locally. Sharing the entire screen is the more reliable way to include the highlight.

## Troubleshooting

| Problem | Try this |
| --- | --- |
| Pointer is running but the settings window is missing | Click **Pointer by AEC Simple** on the taskbar. It may be minimized. You can also open it again from the Start menu. |
| No highlight appears | Open the settings window and check **Pointer circle** or **Click ripples**. Increase visibility by lowering **Transparency**. |
| The shortcut does nothing | Check that **Pointer Monitor** is running in the system tray. If another app already uses the shortcut, choose a different combination in Pointer settings. |
| Pointer does not start when sharing begins | Check the experimental sharing option and that Pointer Monitor is running. Keep the Teams or Zoom sharing controls visible, or use the shortcut. |
| Others cannot see the highlight | Share the entire screen. A single-window share may exclude Pointer's overlay. |

## Update or remove

To update Pointer, run the newer setup file. Your settings are kept.

There is currently no entry in Windows **Installed apps** for removal. To remove Pointer manually:

1. Close Pointer with its **Close** button. Right-click **Pointer Monitor** in the tray and choose **Exit monitor**.
2. Delete `%LOCALAPPDATA%\Programs\Pointer by AEC Simple`.
3. Delete **Pointer by AEC Simple** and **Pointer Monitor** shortcuts from `%APPDATA%\Microsoft\Windows\Start Menu\Programs`.
4. Delete the **Pointer Monitor** shortcut from `%APPDATA%\Microsoft\Windows\Start Menu\Programs\Startup`.
5. If you also want to remove saved preferences, delete `%APPDATA%\MouseHighlighter`.

Made by [AEC Simple](https://aecsimple.com/).
