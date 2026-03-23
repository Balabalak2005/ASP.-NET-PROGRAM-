P.NET Web Forms code review and
Copilot Chat
ASP.NET Web Forms code review and
You said: HTML <%@ Page
HTML     <%@ Page Language="C#" AutoEventWireup="true" CodeBehind="WebForm1.aspx.cs"
Inherits="EX1.WebForm1" %>
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
 <title></title>
</head>
<body>
 <form id="form1" runat="server">
 <div>
 <asp:Label ID="Label1" runat="server" Font-Size="Large"></asp:Label>
 </div>
 </form>
</body>
</html>     BEHIND THE CODE
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
namespace EX1
{
 public partial class WebForm1 : System.Web.UI.Page
 {
 protected void Page_Load(object sender, EventArgs e)
 {
 Label1.Text = DateTime.Now.ToString("dd/MM/yyyy");
 }
 
 }
}         2.<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="WebForm1.aspx.cs"
Inherits="program_2_html_controls.WebForm1" %>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
 <title></title>
 <style type="text/css">
 .style1
 {
 width: 100%;
 }
 .style2
 {
 height: 26px;
 }
 </style>
</head>
<body>
 <form id="form1" runat="server">
 <div>
 
 <table class="style1">
 <tr>
 <td>
 Name:</td>
 <td>
 
<asp:TextBox ID="txtname" runat="server"></asp:TextBox>
 </td>
 </tr>
 <tr>
 <td>
 Street:</td>
 <td>
 
<asp:TextBox ID="txtstreet" runat="server"></asp:TextBox>
 </td>
 </tr>
 <tr>
 <td>
 City:</td>   <td>
 
<asp:TextBox ID="txtcity" runat="server"></asp:TextBox>
 </td>
 </tr>
 <tr>
 <td>
 State:</td>
 <td>
 
<asp:TextBox ID="txtstate runat="server"></asp:TextBox>
 </td>
 </tr>
 <tr>
 <td class="style2">
 </td>
 <td class="style2">
 </td>
 </tr>
 <tr>
 <td>
 &nbsp;</td>
 <td id="displayrow" runat="server">
 &nbsp;</td>
 </tr>
 </table>
 
 </div>
 <asp:Button ID="btnclick" runat="server" Text="Click" OnClick="btnclick_click" />
 <p>
 
<asp:Label ID="lbldisplay"runat="server"></asp:Label>
 </p>
 </form>
</body>
</html>    BEHIND THE CODE:
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
namespace program_2_html_controls
 {
 public partial class WebForm1:System.Web.UI.Page
 {
 protected void Page_Load(object sender, EventArgs e)
 {
 }
 protected void btnclick_click(object sender, EventArgs e)
 {
 string str = "";
 str += txtname.Text + "<br />";
 str += txtstreet.Text + "<br />";
 str += txtcity.Text + "<br />";
 str += txtstate.Text + "<br />";
 displayrow.InnerHtml = str;
 }
 }
}     3 : <%@ Page Title="Home Page" Language="C#" MasterPageFile="~/Site.master"
AutoEventWireup="true"
 CodeBehind="Default.aspx.cs" Inherits="server_controls._Default" %>
<asp:Content ID="HeaderContent" runat="server" ContentPlaceHolderID="HeadContent">
</asp:Content>
<asp:Content ID="BodyContent" runat="server" ContentPlaceHolderID="MainContent">
 <p>
 <br />
 <asp:Label ID="lblname" runat="server" Text="Enter your name"></asp:Label>
 <asp:TextBox ID="txtname" runat="server"></asp:TextBox>
 </p>
 <p>
 <asp:Button ID="btnsubmit" runat="server" Text="Greet me" onclick="btnsubmit_Click"
/>
 <asp:Label ID="lblgreeting" runat="server"></asp:Label>
 </p>
 <p>
 </p>
 <p>
 </p>
 <p>
 </p>
</asp:Content>     BEHIND THE CODE:
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
namespace server_controls
{
 public partial class _Default : System.Web.UI.Page
 {
 protected void Page_Load(object sender, EventArgs e)
 {
 }
 protected void btnsubmit_Click(object sender, EventArgs e)
 {
 lblgreeting.Text = "Hello, " + txtname.Text + "!";
 }
 }
}     4:<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="WebForm1.aspx.cs"
Inherits="program_5_list_controls.WebForm1" %>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
 <title></title>
</head>
<body>
 <form id="form1" runat="server">
 <asp:Label ID="lbllanguage" runat="server"
 Text="Select your programming language:"></asp:Label>
 <br />
 <asp:DropDownList ID="ddllanguage" runat="server">
 <asp:ListItem>Python</asp:ListItem>
 <asp:ListItem>Java</asp:ListItem>
 <asp:ListItem>C++</asp:ListItem>
 </asp:DropDownList>
 <br />
 <br />
 <asp:Label ID="lblhobbies" runat="server" Text="Select your hobbies:"></asp:Label>
 <br />
 <asp:CheckBoxList ID="cblhobbies" runat="server">
 <asp:ListItem>reading</asp:ListItem>
 <asp:ListItem>gaming</asp:ListItem>
 <asp:ListItem>traveling</asp:ListItem>
 </asp:CheckBoxList>
 <br />
 <asp:Label ID="lblcompany" runat="server" Text="Select your company:"></asp:Label>
 <asp:RadioButtonList ID="rblcountry" runat="server">
 <asp:ListItem>India</asp:ListItem>
 <asp:ListItem>USA</asp:ListItem>
 <asp:ListItem>UK</asp:ListItem>
 </asp:RadioButtonList>
 <asp:Button ID="btnsubmit" runat="server" onclick="btnsubmit_Click"
 Text="Submit" />
 <p>
 <asp:Label ID="lblresult" runat="server"></asp:Label>
 </p>
 </form>
</body>
</html>   BEHIND THE CODE:
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
namespace program_5_list_controls
{
 public partial class WebForm1:System.Web.UI.Page
 {
 protected void Page_Load(object sender, EventArgs e)
 {
 }
 protected void btnsubmit_Click(object sender, EventArgs e)
 {
 String selectedLanguage = ddllanguage.SelectedItem.Text.Trim();
 String selectedHobbies = "";
 foreach (ListItem item in cblhobbies.Items)
 {
 if (item.Selected)
 {
 selectedHobbies += item.Text.Trim() + ",";
 }
 }
 if (selectedHobbies.EndsWith(","))
 {
 selectedHobbies = selectedHobbies.Substring(0, selectedHobbies.Length - 2);
 }
 String selectedCountry = rblcountry.SelectedItem != null ? 
rblcountry.SelectedItem.Text.Trim() : "Not selected";
 lblresult.Text = "<b>Selected programming language:</b>+selectedLanguage<br/>" + 
"<b>Selected Hobbies:</b>+selectedHobbies<br/>" + "<b>Selected 
country:</b>+selectedCountry";
 }
 }
}  5:<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="WebForm1.aspx.cs"
Inherits="program_6_rich_controls.WebForm1" %>
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head runat="server">
 <title></title>
</head>
<body>
 <form id="form1" runat="server">
 <div>
 
 <asp:Label ID="lblName" runat="server" Text="Name:"></asp:Label>
 <asp:TextBox ID="txtName" runat="server" CssClass="rich-input"></asp:TextBox>
 <asp:RequiredFieldValidator ID="rfvName" runat="server"
 ControlToValidate="txtName" ErrorMessage="Name Required"
ForeColor="Red"></asp:RequiredFieldValidator>
 <br />
 <br />
 <asp:Label ID="lblEmail" runat="server" Text="Email:"></asp:Label>
 <asp:TextBox ID="txtEmail" runat="server" CssClass="rich-input"></asp:TextBox>
 <asp:RequiredFieldValidator ID="rfvEmail" runat="server"
 ControlToValidate="txtEmail" ErrorMessage="Email Required"
ForeColor="Red"></asp:RequiredFieldValidator>
 <br />
 <asp:RegularExpressionValidator ID="revEmail" runat="server"
 ControlToValidate="txtEmail" ErrorMessage="Invalid Email" ForeColor="Red"
 ValidationExpression="\w+([-+.']\w+)*@\w+([-.]\w+)*\.\w+([-
.]\w+)*"></asp:RegularExpressionValidator>
 <br />
 <br />
 Salary:<asp:TextBox ID="txtSal" runat="server"></asp:TextBox>
 <asp:RangeValidator ID="rvSal" runat="server" BackColor="White"
 ControlToValidate="txtSal" ErrorMessage="Salary must from 10000 to 20000"
 ForeColor="#FF0066" MaximumValue="20000"
MinimumValue="10000"></asp:RangeValidator>
 <br />
 <br />
 Data of joining:<asp:Calendar ID="Calendar1" runat="server"></asp:Calendar>
 <asp:Button ID="btnSave" runat="server" CssClass="rich-button"       Text="Save to File" OnClick="btnSave_Click" />
 <br />
 <br />
 <asp:Label ID="lblMessage" runat="server" ForeColor="Black"></asp:Label>
 <br />
 
 </div>
 </form>
</body>
</html>       BEHIND THE CODE:
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;
namespace program_6_rich_controls
{
 public partial class WebForm1 : System.Web.UI.Page
 {
 protected void Page_Load(object sender, EventArgs e)
 {
 }
 protected void btnSave_Click(object sender, EventArgs e)
 {
 if (Page.IsValid)
 {
 String userData = "Name: {txtName.Text}, Email: {txtEmail.Text}, Salary: 
{txtSalary.Int}, Date: {DateTime.Now}\n";
 //File concept:Append to data.txt
 String filePath = Server.MapPath("~/data.txt");
 System.IO.File.AppendAllText(filePath, userData);
 lblMessage.Text = "Data saved to file successfully!";
 txtName.Text = "";// clear inputs
 txtEmail.Text = "";
 txtSal.Text = "";
 }
 else
 {
 lblMessage.Text = "Please fix validation errors.";
 }
 }
 }
