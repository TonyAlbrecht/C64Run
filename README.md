# C64Run

Double-click a C64 file in Windows Explorer and it runs on your **C64 Ultimate**.

C64Run is a single, small `.exe`: no installer, no runtime, no admin rights needed.

## Features

- **Double-click to run** `.prg`, `.crt`, `.d64`, `.sid` and `.mod` files on the C64 Ultimate.
- **Right-click menu** with a *C64 Ultimate* submenu:
  - Run on C64 Ultimate / Play on C64 Ultimate
  - Mount disk (disk images only, without resetting the C64)
  - Reset, Reboot, Turn off
  - Settings..., Unregister C64Run
- **Experimental:** `.d71`, `.d81`, `.g64` and `.g71` disk images (mounted and started with `LOAD"*",8,1` / `RUN`).

## Requirements

- Windows 10 or 11 (64-bit)
- A C64 Ultimate on your network, with these enabled in the Ultimate's **Network settings**:
  - **Web Remote Control Service** (REST API)
  - **Ultimate DMA Service** (needed for `.d64` files)

## Getting started

1. Download `C64Run.exe` from the [latest release](../../releases/latest) and put it anywhere (e.g. `Documents\C64Run`).
2. Double-click `C64Run.exe`.
> Because the exe isn't code-signed, Windows SmartScreen may warn you the first time you run it. Click **More info → Run anyway**.
3. Enter your C64 Ultimate's IP address (shown in its menu under network settings), and the network password if you set one.
4. Leave `Open supported files with C64Run` ticked and click **Save**.

That's it — double-click any supported file to run it.

## Using the right-click menu

Right-click a supported file and open the **C64 Ultimate** submenu.
On Windows 11 it's under **Show more options** (or hold **Shift** while right-clicking).

Running a file **resets the C64**. *Mount disk* swaps the disk without a reset — handy when a game asks for the next side.

## Changing settings

Run `C64Run.exe` again, or choose **Settings...** from the right-click menu.

If you move `C64Run.exe` to a different folder, open Settings and click **Save** again so Windows points at the new location.

## Uninstalling

Choose **Unregister C64Run** from the right-click menu (or run `C64Run --unregister`), then delete `C64Run.exe`.

## Troubleshooting

| Problem | Fix |
|---|---|
| "Could not reach C64 Ultimate" | Check the IP address and that the C64 Ultimate is on and on the same network. |
| HTTP status 403 | The network password is wrong — the settings dialog will open so you can fix it. |
| `.d64` files fail but `.prg` works | Enable **Ultimate DMA Service** in the Ultimate's network settings. |
| Menu entries missing | Open Settings and click **Save** with the checkbox ticked. |

## License

Free to use and share unmodified. See [LICENSE.txt](LICENSE.txt).

C64Run is not affiliated with or endorsed by Commodore. "Commodore", "C64" and the Commodore logo are trademarks of their respective owners.
