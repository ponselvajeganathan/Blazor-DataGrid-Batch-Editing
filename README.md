# Blazor DataGrid Batch Editing

## Overview

This sample demonstrates how to enable and use batch editing in the Syncfusion Blazor DataGrid. The application displays a collection of order records and allows users to edit multiple cells across different rows before committing all changes together. Batch editing improves data-entry efficiency by letting users perform several add, update, and delete operations before saving them in a single action.

The sample uses the Syncfusion `SfGrid` component with `GridEditSettings` configured for `EditMode.Batch`. Users can modify multiple records and apply or discard all pending changes through the built-in toolbar commands.

## Key Features

- Uses the Syncfusion `SfGrid` component for tabular data presentation and editing.
- Binds data through the `DataSource="@Orders"` property.
- Enables paging with:
  ```razor
  AllowPaging="true"
  ```
- Provides batch editing toolbar actions:
  ```razor
  Toolbar="@(new List<string>() { "Add", "Delete", "Update", "Cancel" })"
  ```
- Configures batch editing using:
  ```razor
  <GridEditSettings
      AllowAdding="true"
      AllowEditing="true"
      AllowDeleting="true"
      Mode="EditMode.Batch">
  </GridEditSettings>
  ```
- Defines `OrderID` as the primary key:
  ```razor
  IsPrimaryKey="true"
  ```

## Prerequisites

- Visual Studio 2022 or later
- .NET SDK compatible with the project's target framework

## How to Run the Project

1. Clone the repository:
   ```bash
   git clone https://github.com/SyncfusionExamples/Blazor-DataGrid-Batch-Editing.git
   ```

2. Open the solution:
   ```text
   BatchEditingSample.sln
   ```

3. Restore NuGet packages.

4. Build the solution.

5. Run the application using Visual Studio 2022 or the .NET CLI:
   ```bash
   dotnet run
   ```

6. Open the application in a browser.

7. Edit multiple cells across different rows.

8. Select **Update** to save all pending changes in a single batch operation or **Cancel** to discard the modifications.

## Project Structure

```text
Blazor-DataGrid-Batch-Editing/
│
├── BatchEditingSample.sln
├── BatchEditingSample.csproj
├── Program.cs
├── App.razor
├── _Imports.razor
│
├── Pages/
│   └── Index.razor
│
├── Data/
├── Shared/
├── Properties/
└── wwwroot/
```

## Support and Feedback
- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- Full documentation on Blazor DataGrid globalization and localization: https://blazor.syncfusion.com/documentation/datagrid/global-local

## License
This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/teamlicense) before using Syncfusion components in your own applications.