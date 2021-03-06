# How-To: Backup my wallet?

## Important General Information

Your`wallet.dat` is standard located in:

 * On windows this is located at `%AppData%\Komodo\VRSC\VRSC.conf`.
 * On linux it is located at `~/.komodo/VRSC/VRSC.conf`.
 * On MacOS it is located at `~/Library/Application Support/Komodo/VRSC`

`verus command "<userinput>"` needs to be entered literally, with `<userinput>` replaced by your specific userdata. So if the text directs you to use for example `"<Public Address>"`, you replace that (including the `<` and `>`) with the address,
so it looks similar to this: `"RYX6RYU3AAvwVCNyNM4cVyGUhSMUPvKs3r"`.


## Procedure
1. Stop verusd. For Windows-Desktop or Agama, just exit and wait for it to close completely. For the linux cli run `./verus stop`, or for the windows cli run `verus stop`.
4. Once your wallet is finished closing make a backup of your `wallet.dat` file somewhere safe. `wallet.dat` is located in the directory listed in the start of this document (see above). To make the backup just copy it to another directory, make sure to leave the original there for the time being.
5. Now restart your wallet by launching Verus Desktop, Agama or running verusd for the CLI.
6. Now we'll export the wallet (this produces a different kind of file from what we did above).

Note: The filename you replace`<mywalletexport>` with, can only contain letters and figures, no other characters, so it **cannot** have an file-extension

 * Verus Desktop:
   Go to `Settings`, `Coin Settings` en click in the textbox shown there.
   Enter `run z_exportwallet <mywalletexport>` en press enter to execute the command.
 * Agama:
   Go to settings, scroll to the bottom and click CLI, select VRSC in that section.
   Then below type `z_exportwallet <mywalletexport>` and click the button below to run it.
 * linux CLI:
   run `./verus z_exportwallet <mywalletexport>`
 * win CLI:
   run `verus z_exportwallet <mywalletexport>`

note: Pay attention to the feedback this command gives you: it will mention the location the backup file is saved.

The exported wallet should be a file called `<mywalletexport>`, standard in the same directory as your `wallet.dat`. Keep this file secure, it has your plaintext private keys. Verify that the file is there and isn't empty.
