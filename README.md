The MVVM FX project targets Windows Forms and Visual Web GUI.

The project focus on providing a development framework based on three libraries:
- Caliburn.Micro MVVM framework
- bound controls library
- general purpose data binding library

The project's main goal is the MVVM framework. Caliburn.Micro is one of the best MVVM frameworks around (some would say it is the best). Based on a partial port from Dan Durland (http://caliburnmicro.codeplex.com/SourceControl/network/forks/ddurland/CaliburnMicroWinForms), the missing features were added, bit by bit.

In order to do proper MVVM, one must use controls that support data binding. Some of the standard Windows Forms controls (or Visual WebGUI controls for that matter) don't comply with this requirement, namely TreeView. The bound controls library fills this gap.

Due to Windows Forms binding shortcomings, a general purpose binding library is instrumental for the Caliburn.Micro port. The MvvmFx.Windows library is based on Truss (http://truss.codeplex.com/) and includes some features that aren't needed for the Caliburn.Micro port. The same source code was used to build MvvmFx.DataBinding, a smaller version of the library, that is stripped off of all method binding parts, like Action or Command binding. Note "Caliburn.Micro does not need an implementation of ICommand because it has Actions which are superior to commands in every way", as Rob Eisenberg puts it (http://caliburnmicro.codeplex.com/discussions/241024).
