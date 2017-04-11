# ReactiveUI.Griffin.Container

Griffin.Container adapter for ReactiveUI.

# Usage
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
