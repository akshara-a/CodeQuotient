# Change all decimal values to int values in a given range in Excel

```vba
Sub ConvertDecimalsToInts()
    Dim rng As Range
    Dim cell As Range

    Set rng = Range("AI2:AI1000")

    For Each cell In rng
        If IsNumeric(cell.Value) Then
            cell.Value = Int(cell.Value)
        End If
    Next cell
End Sub
```
