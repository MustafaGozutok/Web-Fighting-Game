# DOCX'e Dönüştürme Rehberi

## Yöntem 1: Mermaid Diyagramları ile DOCX Oluşturma

1. **Mermaid Diyagramlarını Görsele Çevir:**
   - https://mermaid.live/ sitesine git
   - SoftwareRequirements.md dosyasındaki her mermaid kod bloğunu kopyala
   - Mermaid Live Editor'a yapıştır
   - "Export" > "PNG" veya "SVG" ile kaydet
   - Görselleri proje klasörüne kaydet (örn: `images/diagram1.png`)

2. **Pandoc ile DOCX Oluştur:**
   ```powershell
   # Pandoc yüklü değilse:
   winget install --id JohnMacFarlane.Pandoc
   
   # Dönüştürme:
   pandoc SoftwareRequirements.md -o SoftwareRequirements.docx --reference-doc=custom-reference.docx
   ```

## Yöntem 2: Online Converter Kullanma

1. https://www.markdowntopdf.com/ veya https://products.aspose.app/words/conversion/md-to-docx
2. SoftwareRequirements.md dosyasını yükle
3. DOCX olarak indir
4. Word'de aç, Mermaid kod bloklarına manuel olarak diyagram görselleri ekle

## Yöntem 3: Google Docs Kullanma (En Kolay)

1. Google Drive'a git
2. "New" > "File upload" > SoftwareRequirements.md yükle
3. Dosyaya sağ tık > "Open with" > "Google Docs"
4. Markdown otomatik formatlanacak
5. Mermaid kod bloklarını manuel olarak diyagram görselleriyle değiştir
6. "File" > "Download" > "Microsoft Word (.docx)"

## Mermaid Diyagram Lokasyonları

SoftwareRequirements.md dosyasında şu satırlarda Mermaid diyagramları var:

- **Use Case Diagram:** Satır ~118-130
- **Architecture Diagram:** Satır ~259-300

Her birini mermaid.live'da render edip kaydedebilirsiniz.
