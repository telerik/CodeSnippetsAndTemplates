# RadGrid CodeSnippet shortcuts for Visual Studio

## Table of contents

| Shortcut | Language| Description |
| --- | --- | --- |
| [`radgridneed`](#radgrid-control-with-needdatasource) | HTML | RadGrid control markup with NeedDataSource handler |
| [`radgrid`](#radgrid-control-with-sqldatasource) | HTML | RadGrid control markup with SqlDataSource|
| [`needsource`](#cs-needsource-event-handler-with-dummy-data) | C# | RadGrid NeedSource event handler with DataTable with dummy data in C# |
| [`vbneedsource`](#vb-needsource-event-handler-with-dummy-data) | VB | RadGrid NeedSource event handler with DataTable with dummy data in VB|

## Markup

### RadGrid control with NeedDataSource
- shortcut: radgridneed
- filename: RadGridNeedSourceMarkup.snippet
- default destination: 'C:\Users\{USERNAME}\Documents\Visual Studio 2015\Code Snippets\Visual Web Developer\My HTML Snippets'

<details>
<summary>Generated code</summary>

```html
<telerik:RadGrid ID="RadGrid1" runat="server" AllowPaging="True" CellSpacing="0"
    GridLines="None" Width="800px" OnNeedDataSource="RadGrid1_NeedDataSource">
    <MasterTableView AutoGenerateColumns="False" DataKeyNames="OrderID">
        <Columns>
            <telerik:GridBoundColumn DataField="OrderID" DataType="System.Int32"
                FilterControlAltText="Filter OrderID column" HeaderText="OrderID"
                ReadOnly="True" SortExpression="OrderID" UniqueName="OrderID">
            </telerik:GridBoundColumn>
            <telerik:GridDateTimeColumn DataField="OrderDate" DataType="System.DateTime"
                FilterControlAltText="Filter OrderDate column" HeaderText="OrderDate"
                SortExpression="OrderDate" UniqueName="OrderDate">
            </telerik:GridDateTimeColumn>
            <telerik:GridNumericColumn DataField="Freight" DataType="System.Decimal"
                FilterControlAltText="Filter Freight column" HeaderText="Freight"
                SortExpression="Freight" UniqueName="Freight">
            </telerik:GridNumericColumn>
            <telerik:GridBoundColumn DataField="ShipName"
                FilterControlAltText="Filter ShipName column" HeaderText="ShipName"
                SortExpression="ShipName" UniqueName="ShipName">
            </telerik:GridBoundColumn>
            <telerik:GridBoundColumn DataField="ShipCountry"
                FilterControlAltText="Filter ShipCountry column" HeaderText="ShipCountry"
                SortExpression="ShipCountry" UniqueName="ShipCountry">
            </telerik:GridBoundColumn>
        </Columns>
    </MasterTableView>
</telerik:RadGrid>
```

</details>

### RadGrid control with SqlDataSource
- shortcut: radgrid
- filename: RadGridSqlDataSource.snippet
- default destination: 'C:\Users\{USERNAME}\Documents\Visual Studio 2015\Code Snippets\Visual Web Developer\My HTML Snippets'

<details>
<summary>Generated code</summary>

```html
<telerik:RadGrid ID="RadGrid1" runat="server" AllowPaging="True" CellSpacing="0"
    DataSourceID="SqlDataSource1" GridLines="None" Width="800px">
    <MasterTableView DataSourceID="SqlDataSource1" AutoGenerateColumns="False"
        DataKeyNames="OrderID" >
        <Columns>
            <telerik:GridBoundColumn DataField="OrderID" DataType="System.Int32"
                FilterControlAltText="Filter OrderID column" HeaderText="OrderID"
                ReadOnly="True" SortExpression="OrderID" UniqueName="OrderID">
            </telerik:GridBoundColumn>
            <telerik:GridDateTimeColumn DataField="OrderDate" DataType="System.DateTime"
                FilterControlAltText="Filter OrderDate column" HeaderText="OrderDate"
                SortExpression="OrderDate" UniqueName="OrderDate">
            </telerik:GridDateTimeColumn>
            <telerik:GridNumericColumn DataField="Freight" DataType="System.Decimal"
                FilterControlAltText="Filter Freight column" HeaderText="Freight"
                SortExpression="Freight" UniqueName="Freight">
            </telerik:GridNumericColumn>
            <telerik:GridBoundColumn DataField="ShipName"
                FilterControlAltText="Filter ShipName column" HeaderText="ShipName"
                SortExpression="ShipName" UniqueName="ShipName">
            </telerik:GridBoundColumn>
            <telerik:GridBoundColumn DataField="ShipCountry"
                FilterControlAltText="Filter ShipCountry column" HeaderText="ShipCountry"
                SortExpression="ShipCountry" UniqueName="ShipCountry">
            </telerik:GridBoundColumn>
        </Columns>            
    </MasterTableView>
</telerik:RadGrid>
<asp:SqlDataSource ID="SqlDataSource1" runat="server"
    ConnectionString="<%$ ConnectionStrings:ConnectionString %>"
    SelectCommand="SELECT [OrderID], [OrderDate], [Freight], [ShipName], [ShipCountry] FROM [Orders]"></asp:SqlDataSource>
```

</details>


## Code-behind - C#

### CS NeedSource event handler with dummy data
- shortcut: needsource
- filename: GridNeedSourceDummyData.snippet
- default destination: 'C:\Users\{USERNAME}\Documents\Visual Studio 2015\Code Snippets\Visual C#\My Code Snippets'

<details>
<summary>Generated code</summary>

```cs
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

</details>

## Code-behind - VB

### VB NeedSource event handler with dummy data 
- shortcut: vbneedsource
- filename: GridVBNeedDataSource.snippet
- default destination: 'C:\Users\{USERNAME}\Documents\Visual Studio 2015\Code Snippets\Visual Basic\My Code Snippets'

<details>
<summary>Generated code</summary>

```vb
Protected Sub RadGrid1_NeedDataSource(sender As Object, e As GridNeedDataSourceEventArgs)
	RadGrid1.DataSource = GetGridSource()
End Sub
Private Function GetGridSource() As DataTable
	Dim dataTable As New DataTable()

	Dim column As New DataColumn()
	column.DataType = Type.[GetType]("System.Int32")
	column.ColumnName = "OrderID"
	dataTable.Columns.Add(column)

	column = New DataColumn()
	column.DataType = Type.[GetType]("System.DateTime")
	column.ColumnName = "OrderDate"
	dataTable.Columns.Add(column)

	column = New DataColumn()
	column.DataType = Type.[GetType]("System.Decimal")
	column.ColumnName = "Freight"
	dataTable.Columns.Add(column)

	column = New DataColumn()
	column.DataType = Type.[GetType]("System.String")
	column.ColumnName = "ShipName"
	dataTable.Columns.Add(column)

	column = New DataColumn()
	column.DataType = Type.[GetType]("System.String")
	column.ColumnName = "ShipCountry"
	dataTable.Columns.Add(column)

	Dim PrimaryKeyColumns As DataColumn() = New DataColumn(0) {}
	PrimaryKeyColumns(0) = dataTable.Columns("OrderID")
	dataTable.PrimaryKey = PrimaryKeyColumns

	For i As Integer = 0 To 80
		Dim row As DataRow = dataTable.NewRow()
		row("OrderID") = i + 1
		row("OrderDate") = DateTime.Now
		row("Freight") = (i + 1) + (i + 1) * 0.1 + (i + 1) * 0.01
		row("ShipName") = "Name " & (i + 1)
		row("ShipCountry") = "Country " & (i + 1)

		dataTable.Rows.Add(row)
	Next

	Return dataTable
End Function
```

</details>
