# Visual-Studio-Multi-Tier-Service-Bus-Queue
This app demonstrates Visual Studio Multi Tier Azure Service Bus. it Includes Service Bus Namespace, Frontend App to accept online orders, and backend app to process orders passed to the service bus namespace queue


### To use this demo you need to do the following:

1. Create Azure ServiceBus Namespace.
2. After the ServiceBus Namespace is created navigate to it.
3. From the left pane, under Settings, select Share Access Policies
4. Then select RootManageSharedAccessKey.
5. Copy both Primary ConnectionString and Primary AccessKey to a notepad.
6. Clone the repository to Visual Studio and got to Solution Explorer.
7. In Solution Explorer, Expand MultiTierApp->Roles and Right-Click OrderProcessingRole and Select Properties.
8. In the Peroperties Windows, under Settings, Change the value of the Microsoft.Servicebus.ConnectionString to add the one you copied in step 5.
9. In Solution Explorer, Under FrontendWebRole Solution, double click QueueConnector.cs and change the following:
        * public const string Namespace = ___"Add your ServiceBus Namespace NAME here"___
        * "RootManageSharedAccessKey", ___"Add your ServiceBus Namespace PrimaryKey here")___
10. Save the project and close Visual Studio.
11. Start Visual Studio as Administrator by Right-Click on Visual Studio icon and Run As Administrator.
12. Load your project and press F5 wich will run the app and start Micsoft Azure Emulator in your Taskbar.
13. To view progress, Create orders in the web browser page, right-click Compute Emulator in your Tasbar and select Show Compute Emulator UI to watch the progress.

Enjoy :)
