# HtmlRendererCore.PdfSharp
HtmlRendererCore. Pdfsharp implements the standard class library from HTML to PDF based on the pdfsharpcore class library. 
The project is rewritten based on the j-petty project. https://github.com/j-petty/HtmlRendererCore 。

This library offers Html to Pdf parsing for .Net Core projects using [PdfSharpCore](https://github.com/ststeiger/PdfSharpCore).

Future updates will be focused at cleaning up the codebase and offering support for more advanced HTML rendering. Public pull requests welcome.

## Example usage 

### Generate PDF from HTML

```cs
var pdf = PdfGenerator.GeneratePdf(html, PdfSharpCore.PageSize.A4);
```

### Generating Base64 PDF from HTML

```cs
var result = string.Empty;

using (var stream = new MemoryStream())
{
    var pdf = PdfGenerator.GeneratePdf(html, PdfSharpCore.PageSize.A4);

    pdf.Save(stream);

    result = Convert.ToBase64String(stream.ToArray());
}
```

## Documentation

**HtmlRenderer:** https://archive.codeplex.com/?p=htmlrenderer

**PdfSharpCore:** https://github.com/ststeiger/PdfSharpCore

**j-petty HtmlRendererCore:** https://github.com/j-petty/HtmlRendererCore

## License


Copyright (c) 2022 BigCat

MIT

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
