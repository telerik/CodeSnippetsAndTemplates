# RadGrid CodeSnippet shortcuts for Visual Studio

## Table of contents

### TODO:

## Markup

### TODO:

## Code-behind - C#

### NeedSource event handler with dummy data
- shortcut: needsource
- filename: GridNeedSourceDummyData.snippet
- default destination: 'C:\Users\{USERNAME}\Documents\Visual Studio 2015\Code Snippets\Visual C#\My Code Snippets'
- generated code: 
```
protected void RadGrid1_NeedDataSource(object sender, GridNeedDataSourceEventArgs e)
{
    RadGrid1.DataSource = GetGridSource(); 
}
private DataTable GetGridSource()
{
    DataTable dataTable = new DataTable();

    DataColumn column = new DataColumn();
    column.DataType = Type.GetType("System.Int32");
    column.ColumnName = "OrderID";
    dataTable.Columns.Add(column);

    column = new DataColumn();
    column.DataType = Type.GetType("System.DateTime");
    column.ColumnName = "OrderDate";
    dataTable.Columns.Add(column);

    column = new DataColumn();
    column.DataType = Type.GetType("System.Decimal");
    column.ColumnName = "Freight";
    dataTable.Columns.Add(column);

    column = new DataColumn();
    column.DataType = Type.GetType("System.String");
    column.ColumnName = "ShipName";
    dataTable.Columns.Add(column);

    column = new DataColumn();
    column.DataType = Type.GetType("System.String");
    column.ColumnName = "ShipCountry";
    dataTable.Columns.Add(column);

    DataColumn[] PrimaryKeyColumns = new DataColumn[1];
    PrimaryKeyColumns[0] = dataTable.Columns["OrderID"];
    dataTable.PrimaryKey = PrimaryKeyColumns;

    for (int i = 0; i <= 80; i++)
    {
        DataRow row = dataTable.NewRow();
        row["OrderID"] = i + 1;
        row["OrderDate"] = DateTime.Now;
        row["Freight"] = (i + 1) + (i + 1) * 0.1 + (i + 1) * 0.01;
        row["ShipName"] = "Name " + (i + 1);
        row["ShipCountry"] = "Country " + (i + 1);

        dataTable.Rows.Add(row);
    }

    return dataTable;
}
```

## Code-behind - VB

### TODO:
