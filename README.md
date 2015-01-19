# Heloy
Raino
unit Unit1;

{$mode objfpc}{$H+}

interface

uses
  Classes, SysUtils, FileUtil, Forms, Controls, Graphics, Dialogs, StdCtrls,
  Buttons;

type

  { TForm1 }

  TForm1 = class(TForm)
    Button1: TButton;
    Button2: TButton;
    Button3: TButton;
    Button4: TButton;
    Edit1: TEdit;
    Edit2: TEdit;
    Edit3: TEdit;
    Label1: TLabel;
    Label2: TLabel;
    Label3: TLabel;
    procedure Button1Click(Sender: TObject);
    procedure Button2Click(Sender: TObject);
    procedure Button3Click(Sender: TObject);
    procedure Button4Click(Sender: TObject);
    procedure Label3Click(Sender: TObject);
  private
    { private declarations }
  public
    { public declarations }
  end;

var
  Form1: TForm1;

implementation

{$R *.lfm}

{ TForm1 }

procedure TForm1.Label3Click(Sender: TObject);
begin

end;

procedure TForm1.Button1Click(Sender: TObject);
begin
  Edit3.Text:=FloattoStr(StrtoFloat(Edit1.Text)+ StrtoFloat(Edit2.Text));
end;

procedure TForm1.Button2Click(Sender: TObject);
begin
  Edit3.Text:=FloattoStr(StrtoFloat(Edit1.Text)* StrtoFloat(Edit2.Text));
end;

procedure TForm1.Button3Click(Sender: TObject);
begin
  Edit3.Text:=FloattoStr(StrtoFloat(Edit1.Text)/ StrtoFloat(Edit2.Text));
  if StrtoFloat(edit2.Text)=0 then edit3.text:='деление на 0' else ;
end;

procedure TForm1.Button4Click(Sender: TObject);
begin
  edit3.Text:='0';
  edit2.Text:='0';
  edit1.Text:='0';
end;

end.
                                      
