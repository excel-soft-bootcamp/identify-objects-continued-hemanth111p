Data Binding

User can bind the data with the controls of the forms. This process is known as data binding.

 There are two types of data binding in ASP.NET 

1. simple data binding 
2.  declarative data binding.

1.simple data binding :

-In simple data binding, the control is bounded to a data set. 
-The properties of the control are used for binding with the value. 
-Depending on the control to be bounded, the binding’s property is set.

example:

```
SimpleDataBinding.aspx:
 <asp:TextBox ID="txtname" runat="server"></asp:TextBox><br />
            <asp:Button ID="Button1" runat="server" Text="Show" OnClick="Button1_Click" /><br />
            <asp:Label ID="Label1" runat="server" Text="<%# UserName %>"></asp:Label>

SimpleDataBinding.aspx.cs:
public string UserName;
protected void Show_Click(object sender, EventArgs e)
    {
        UserName = txtname.Text;
        this.DataBind();
    }
```



2.Declarative data binding:

-The process of binding a component like listbox, DataGrid, record list with the dataset is known as declarative binding. 
-When there is more than one element in the database, the declarative binding is used.

Example:

```
 DeclarativeDataBinding.aspx:
 <asp:ListBox ID="ListBox1" runat="server"></asp:ListBox>
        <br />
        <asp:Button ID="Button1" runat="server" OnClick="Button1_Click" Text="Show" />
        
 DeclarativeDataBinding.aspx.cs:
  protected void Button1_Click(object sender, EventArgs e)
    {
        List<String> list = new List<string>();
        list.Add("Bengalore");
        list.Add("Mysore");
        list.Add("Chamarajanagar");
        ListBox1.DataSource = list;
        this.DataBind();
    }
```

