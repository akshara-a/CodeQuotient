# VBA Script to Write the Same Value for a Range of Cells in a Column

This VBA script writes the value from a specific cell (B6 and C6) to a range of cells in the same columns (B7:B1001 and C7:C1001).

## VBA Code

```vba
Sub FillValue()
    Dim valueToCopyB As Variant
    valueToCopyB = Range("B6").Value
    Range("B7:B1001").Value = valueToCopyB
    
    Dim valueToCopyC As Variant
    valueToCopyC = Range("C6").Value
    Range("C7:C1001").Value = valueToCopyC
End Sub


# Steps - 
Press Alt + F11 to open the VBA editor.
In the VBA editor, go to Insert > Module to create a new module.
Copy and paste the provided VBA code into the new module.
Press F5 to run the macro directly from the VBA editor, or you can close the VBA editor and run the macro from Excel.
