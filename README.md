<div align="center">

## Print HTML from Visual Basic


</div>

### Description

The purpose of this article is to explain how to get the WebBrowser to print (i.e. there is no standard print method)
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Philip Leitch](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/philip-leitch.md)
**Level**          |Beginner
**User Rating**    |4.3 (17 globes from 4 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[Internet/ HTML](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/internet-html__1-34.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/philip-leitch-print-html-from-visual-basic__1-37377/archive/master.zip)





### Source Code

<p>I was creating a form to be printed by HTML, then, after creating the form, realised that I didn’t know how to print the HTML. I looked into it further and found some obscure way in MSDN and some message boards to set focus (through Windows API) to my HTML WebBrowser control and send it a Control P key. The problem is that that only brings up a print dialogue. I didn’t even want to show the HTML form, let alone ask the user to select which printer. I searched further and found a workable solution. Here it is:</p>
<p></p>
<p></p>
<p>frmHTML.WebBrowser1.Navigate(&quot;C:\temp\Request.htm&quot;)</p>
<p>frmHTML.WebBrowser1.ExecWB OLECMDID_PRINT, OLECMDEXECOPT_DONTPROMPTUSER, 0, 0</p>

