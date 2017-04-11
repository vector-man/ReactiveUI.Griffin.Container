# ReactiveUI.Griffin.Container

Griffin.Container adapter for ReactiveUI.

# Usage

1. Install Griffin.Container and ReactiveUI.

2. Add the file GriffinDependancyResolver.cs to your ReactiveUI project.

3. Finally, use it like this
    
    internal static class Program
    {
        /// <summary>
        /// The main entry point for the application.
        /// </summary>
        [STAThread]
        private static void Main()
        {
          var container = new ContainerRegistrar();
          Locator.Current = new GriffinDependancyResolver(container);
          Application.Run((MainView)Locator.CurrentMutable.GetService<IMainView>());
        }
     }
