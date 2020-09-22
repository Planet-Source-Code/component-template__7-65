<div align="center">

## Component Template


</div>

### Description

Here is an example showing how to use the Component Template. You will find it under 'Component' on the Delphi menu.

Component Templates are very handy, yet very simple to use.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[N/A](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/empty.md)
**Level**          |Beginner
**User Rating**    |3.7 (11 globes from 3 users)
**Compatibility**  |Delphi 5, Delphi 4, Pre Delphi 4
**Category**       |[Custom Controls/ Forms/ Menus](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/custom-controls-forms-menus__7-4.md)
**World**          |[Delphi](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/delphi.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/component-template__7-65/archive/master.zip)





### Source Code

```
irst start with a blank Form.
Add a Panel, and set Panel1.Align to alTop.
Drop 4 Button components on Panel1 in a row.
Put these names in the Buttons Captions:
 OpenSave
Clear
Exit
In that order.
Next drop a StatusBar component on the Form, this should be aligned to alBottom.
Then drop a TMemo on the Form, and set its Align Property in the Object Inspector to alClient.
Next drop a OpenDialog component on the Form and a SaveDialog component.
Double-Click on the first Button, this is the Button with Open as its caption.
Then enter this code (the code between Begin & End;):
procedure TForm1.Button1Click2(Sender: TObject);
begin
 if OpenDialog1.Execute then
 Memo1.Lines.LoadFromFile(OpenDialog1.FileName);
end;Double-Click on the second Button (The Save button) and enter this
code:
procedure TForm1.Button2Click2(Sender: TObject);
begin
 if SaveDialog1.Execute then
  begin
   Memo1.Lines.SaveToFile(SaveDialog1.FileName);
  end;
end;Double-Click on the third Button and enter this code:
procedure TForm1.Button3Click2(Sender: TObject);
begin
 Memo1.Clear;
end;Double-Click on the forth button and add this code:
procedure TForm1.Button4Click2(Sender: TObject);
begin
 Close;
end;Click on the OpenDialog1 component and in the Object Inspector double-click on Filter, then put in this text:
TXT  *.txt
All files *.*Do the same for the SaveDialog component.
Here comes the nifty part.
Go up to Edit in the Delphi menu and then
click on Select All then...
Click on Component in the Delphi file menu, then click on Create Component Template...
Type in the name you wish to use for the component template.
You can leave the Palette page name as Template.
And pick an icon for the new Template.
Click on OK and that's it.
Start a new project, go to the Template palette and click on your new component template.
Drop this on the Form and run the program.
And there you have it, an instant text editor.
You can set the StatusBar anyway you want.Just another amazing thing you can do with Borland's Delphi!
```

