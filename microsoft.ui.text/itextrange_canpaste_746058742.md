---
-api-id: M:Microsoft.UI.Text.ITextRange.CanPaste(System.Int32)
-api-type: winrt method
---

<!-- Method syntax
public bool CanPaste(System.Int32 format)
-->

# Microsoft.UI.Text.ITextRange.CanPaste

## -description
Determines whether the Clipboard contains content that can be pasted, using a specified format, into the current text range.

## -parameters
### -param format
The clipboard format. Zero represents the best format, which usually is Rich Text Format (RTF), but CF_UNICODETEXT and other formats are also possible. The default value is zero.

## -returns
True if the Clipboard content can be pasted into the text range in the specified format, and otherwise false.

## -remarks

## -examples

## -see-also
