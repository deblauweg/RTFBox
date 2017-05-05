# RTFBox

This is the short explication of the license what you can do, can’t do and must do:
https://tldrlegal.com/license/eclipse-public-license-1.0-(epl-1.0)

How to add this in your application?

For the parser you need:
- clsRTFBox_Data
	Events
		FillFunctionValue(strFunction As String, ByRef strValue As String) As Boolean
		GetDefaultStyle(ByRef strFont As String, ByRef iFontSize As Integer, ByRef bBold As Boolean, ByRef bItalic As Boolean, ByRef bUnderline As Boolean)
	Methods
		GetHTML() As String
		GetRTF() As String
		GetText() As String
		InsertRTF(iPos As Integer, strRTF As String)
		InsertText(iPos As Integer, strText As String)
		SetRTF(strValue As String)
		SetText(strValue As String)		
- clsRTFBox_Paragraph
- clsRTFBox_Picture

The control itself is 
- clsRTFBox
	Events
		FillFunctionValue(strFunction As String, ByRef strValue As String) As Boolean
		GetDefaultStyle(ByRef strFont As String, ByRef iFontSize As Integer, ByRef bBold As Boolean, ByRef bItalic As Boolean, ByRef bUnderline As Boolean)
		GetFunctions(ByRef strArrFunctions() As String, ByRef strArrNames() As String)
		GotFocus()
		KeyDown(strKey As String) As Boolean
		LostFocus()
		MouseDown(iX As Integer, iY As Integer) As Boolean
		TextChanged() 
	Methods
		DrawRTF_GetArray(iWidth As Integer, iHeightFirstPage As Integer, iHeightOtherPages As Integer) As Picture()
		GetHtml() As String
		GetRTF() As String
		GetText() As String
		Print() (This part is not ready)
	Properties
		Language As String
		ReadOnly As Boolean
		Value As String

You’re able to enable and disable these parts by setting their Constants before compiling:
- clsRTFBox_Data.ALLOW_CHECKBOX
- clsRTFBox_Data.ALLOW_EXTRALINESTYLES
- clsRTFBox_Data.ALLOW_NSTOUCHBAR
	This part is not ready, the icons on the toucher are readonly
	For this you’ll need these MBS plugins:
		MBS Xojo Cocoa Plugin
		MBS Xojo CocoaBase Plugin
		MBS Xojo CocoaControls Plugin
		MBS Xojo CocoaExtras Plugin
		MBS Xojo Controls Plugin
		MBS Xojo Leopard Plugin
		MBS Xojo Lion Plugin
		MBS Xojo Mac Plugin
		MBS Xojo Mac64bit Plugin
		MBS Xojo MacOSX Plugin
		MBS Xojo MacOSXCF Plugin
		MBS Xojo MacOSXCG Plugin
		MBS Xojo Main Plugin
		MBS Xojo SnowLeopard Plugin
	And Include this class in your project:
		RTF_NSTouchBarMBS
- clsRTFBox_Data.ALLOW_PAGEBREAK
- clsRTFBox_Data.ALLOW_PICTURES
- clsRTFBox_Data.ALLOW_SPELLCHECKER
	For this you’ll need this plugin from Bob Keeney:
		BKSSpellChecker
- clsRTFBox_Data.ALLOW_TABLES

If you like this control, it saved you a lot of time, use these classes, 
and you would like to show appreciation somehow,
My PayPal link is: https://paypal.me/GinoDeblauwe

