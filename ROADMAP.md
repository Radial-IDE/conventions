Roadmap
=======
Contributors may use this roadmap for finding features that need to be implemented. Items are displayed as `[Module] Name [Implementer]: Description`. Contributors may submit a pull request whenever they wish to claim implementing a feature listed here including their username and link to the respective branch.

Stage 0:
--------
This stage focuses on GUI related tasks that do not directly influence any of the later stages. These tasks can be done at any point.
 - **`[GUI]` Command Line Arguments [N/A]:** The IDE should display available command line arguments with a short description when prompted to. It should also be trivial to add new arguments.
 - **`[GUI]` IPC [N/A]:** IPC is necessary to tell if there is another instance running. In particular, when users open a file they may expect it to be opened in the current instance. A command line flag should be available to disable this specific functionality.
 - **`[GUI]` Preferences [N/A]:** A preferences dialog would exist as an easy way to edit options. This would require creating a file type that stores preferences, which would preferably in TOML format. Note, that the GUI should have both a portable mode and a non-portable mode which determines where it looks for files.
   - **`[GUI]` Skins [N/A]:**  Skins exist as themes for the entire application. Skins should be settable via command line arguments in case the user accidently sets an unusable theme and would like to revert to another skin. Skins should be locatable under `themes/skins/[Skin Name]`.
   - **`[GUI]` Icons [N/A]:** A standard icon set should be available for GUI plugins to use. Icon sets should be available under `themes/icons/[Icon Set Name]`.
 - **`[GUI]` Detachable Workspace [N/A]:** Allow users to detach editors from their current windows and move them to their own windows.
 - **`[GUI]` Auto-update [N/A]:** The application should update itself when it is opened. It should query a server in another thread (or maybe even begin another process) and begin downloading updates, with it being able to resume an update if it started previously but was incomplete. Finally, it must validate the download, possibly using SHA-256. A macro should be used to enable updating (disabled by default so developers don't get their executable changed).
