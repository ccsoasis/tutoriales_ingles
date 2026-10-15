# Definition of Recorders

Each *Tutorial* includes a series of Panels consisting of Recorders, that the author estimates adequate for the configuration. This series is grouped below the (single) "*StripRecorders*" element.

Example:

&lt;*StripRecorderPanels* backColor="1" borderColor="0"&gt;

&lt;*Panel* name="Pitch, Potencias, Freno, RPMs, Viento" description="Panel general"&gt;

&lt;*Recorder* type="A" name="Pitch" maxValue="+55" minValue="-5" height="120"&gt;

&lt;*Signal* type="A" name="Controller.Control.PitchOut" color="0,0,255" /&gt;

&lt;Signal type="A" name="Nacelle.DriveTrain.PitchNacelleOut" color="0,128,0"/&gt;

&lt;*MarkLine* value="90.0" label=" 90" alphaValue="130" color="0,0,0"/&gt;

&lt;*MarkLine* value="45.0" label=" 45" alphaValue="130"/&gt;

&lt;*MarkLine* value="-5.0" label="-5" alphaValue="130"/&gt;

&lt;*MarkLine* value="0.0" label="0" alphaValue="130"/&gt;

&lt;*MarkLine* value="30.0" label=" 30" alphaValue="130"/&gt;

&lt;*MarkLine* value="20.0" label=" 20" alphaValue="130"/&gt;

&lt;*MarkLine* value="10.0" label=" 10" alphaValue="130"/&gt;

&lt;/*Recorder*&gt;

&lt;*Recorder* type="A" name="Potencias" maxValue="1700000" minValue="-10" height="120"&gt;

&lt;*Signal* type="A" name="Nacelle.DFIGB2B.GridActivePower" color="0,128,0" /&gt;

&lt;*Signal* type="A" name="Nacelle.DriveTrain.ActualWindPowerOut"/&gt;

&lt;*MarkLine* value="0" label="0" alphaValue="130"/&gt;

&lt;*MarkLine* value="500000" label="500kW" alphaValue="130"/&gt;

&lt;*MarkLine* value="1000000" label="1MW" alphaValue="130"/&gt;

&lt;*MarkLine* value="1500000" label="1.5MW" alphaValue="130"/&gt;

&lt;/*Recorder*&gt;

&lt;*Recorder* type="D" name="Frenos" height="60"&gt;

&lt;*Signal* type="D" name="Nacelle.Braking.BrakeReleasedOut"/&gt;

&lt;/*Recorder*&gt;

&lt;/*Panel*&gt;

&lt;/*StripRecorderPanels*&gt;

## Description of Elements Associated with StripRecorders

### StripRecorders

This element has two "properties" or "attributes"

| **Property** | **Description** |
|---|---|
| *backColor* | This property determines the Panels background color. The possible ways of specifying this color are the following: ="0" : black background color. ="1" : white background color. ="R,G,B" , where R, G and B are integer values between 0 and 255. Example: with "200,200,200" the following background color is obtained. ![](<lib/Striprecorder bf 200200200.jpg>) |
| *borderColor* | ="0" (Future use). |

### Panel

This element has two properties "**name**" and "**description**", both text. Each panel corresponds to a synoptic. It can contain one or more "*Recorder*" elements.

### Recorder

This element can contain one or more "*Signal*" elements and zero, one or more "*MarkLine*" elements. It has the following properties:

| **Property** | **Description** |
|---|---|
| *type* | Required. Can be "A" if you want to represent analog signals, or "D" if they are digital. |
| *name* | Required. Used for identification. |
| *maxValue* | Required. Upper value of the vertical axis of values. |
| *minValue* | Required. Lower value of the vertical axis. |
| *height* | Required. Height of the Recorder in pixels. |
| *scaleMode* | Optional. The values can be "*lin*" or "*log*". The default value is "lin". If "*lin*", the signal value scale is linear. If "*log*", the signal value scale is logarithmic. |

### Signal

This element specifies one of the signals to be represented in the "Recorder" element within which it is defined. The color can be chosen.

| **Property** | **Description** |
|---|---|
| *type* | Required. Can be "A" if you want to represent analog signals, or "D" if they are digital. |
| *name* | Required. Must correspond to the name of a valid "signal". See [Synoptic for editing Signals and Connections](EstructuraAplicLdPSinopticoSenCo.md). |
| *color* | Required. ="R,G,B", where R, G, and B are integer values between 0 and 255. |

### MarkLine

This element displays a horizontal line corresponding to a possible value of the signals represented in the "Recorder" element where it is defined. The color and transparency can be changed. The associated text is displayed to the right of the ordinate axis.

| **Property** | **Description** |
|---|---|
| *value* | Required. Associated value. Examples: "10.0", "-15.0", "1e-4", "-2e+8". |
| *label* | Required. Text displayed to the right of the y-axis. |
| *color* | Required. ="R,G,B", where R, G, and B are integer values between 0 and 255. |
| *alphaValue* | Required. Value between 0 and 255 corresponding to the degree of transparency of the horizontal line drawn. 0 is completely transparent. 255 is not transparent. |
