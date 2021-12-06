# ICommand

Solution demonstrates how ICommand interface works in WPF. 

```cs
using System;
using System.Windows.Input;

namespace wpf_icommand.ViewModels.Commands
{
    public class MessageCommand : ICommand
    {
        public event EventHandler CanExecuteChanged;
        private Action _execute;

        public MessageCommand(Action execute)
        {
            _execute = execute;
        }

        public bool CanExecute(object parameter)
        {
            return true;
        }

        public void Execute(object parameter)
        {
            _execute.Invoke();
        }
    }
}
 ```

Link to documentation -> [docs.microsoft.com](https://docs.microsoft.com/en-us/dotnet/api/system.windows.input.icommand?view=net-6.0)
