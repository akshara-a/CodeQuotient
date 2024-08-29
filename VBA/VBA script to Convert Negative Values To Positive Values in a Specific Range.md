# VBA script to Convert Negative Values To Positive Values in a Specific Range

```vba
Sub ConvertNegativesToPositives()
    Dim rng As Range
    Dim cell As Range

    ' Set the range to your specific range
    Set rng = Range("AI2:AI10006")

    For Each cell In rng
        If IsNumeric(cell.Value) And cell.Value < 0 Then
            cell.Value = Abs(cell.Value)
        End If
    Next cell
End Sub
```

{% include base_content.md %}
