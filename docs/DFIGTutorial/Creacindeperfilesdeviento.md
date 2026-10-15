# Wind profile creation

The content of the wind gust files (with "\*.wgt" extension) has a specific binary format, which corresponds to the following example program. This VBA code is contained in the file "CreateWGTFile.xlsm".

-------------------------------------------

Option Explicit

Public Type **WindGustEntry**

Time As Double

Wind As Double

End Type

Public Sub **CreateWGTfile**(iFileName As String, iRange As Range)

Dim I As Integer, fileNumber As Integer

Dim nWGEntry As WindGustEntry

fileNumber = FreeFile(0)

Open iFileName For Random As #fileNumber Len = Len(nWGEntry)

For I = 2 To UBound(iRange.Value2)

nWGEntry.Time = iRange.Value2(I, 1)

nWGEntry.Wind = iRange.Value2(I, 2)

Put #fileNumber, I - 1, nWGEntry

Next I

Close #fileNumber

End Sub

---------------------------------

![](<lib/Excel creacion fichero rafagas.jpg>)

The Excel 2007 workbook "*CreateWGFfile.xlsm*" contains the previous code and a form ("UserForm1") that contains the button that creates the file with the name and location shown, and whose content corresponds to the selected zone, which also has an associated graph, so that by modifying that zone the repercussion can be seen directly in the graph.

The values saved in the created file correspond to those associated with the "Range" "WindGust".

For the wind gust files to be taken into account they must be placed in the "*..\\WindFarmSimulator\\windgusts*" directory.
