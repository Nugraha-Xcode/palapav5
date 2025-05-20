---
title: 'Panduan Pengisian XML'
---

::::info
**Panduan Penyesuaian Template Metadata XML**
**Geoportal Palapa 5.0**
::::



#  Pendahuluan

Berikut adalah template metadata XML yang bisa disesuaikan dengan kebutuhan Anda. (Dokumen ini siap digunakan, ganti teks yang diberi tanda [ ] sesuai kebutuhan)

[Download Template Metadata](https://drive.google.com/file/d/1aSy587iMrlEeg9QSdtW0P13w6lYL6ogG/view?usp=sharing)

# 1. Informasi Dasar Metadata
```xml
<gmd:MD_Metadata xmlns:gml="http://www.opengis.net/gml/">
  <gmd:fileIdentifier>
    <gco:CharacterString>[IDENTIFIER_UNIK_DATASET]</gco:CharacterString>
  </gmd:fileIdentifier>
  <gmd:language>
    <gmd:LanguageCode codeList="./resources/codeList.xml#LanguageCode" codeListValue="eng">eng</gmd:LanguageCode>
  </gmd:language>
  <gmd:characterSet>
    <gmd:MD_CharacterSetCode codeList="http://www.isotc211.org/2005/resources/Codelist/gmxCodelists.xml#MD_CharacterSetCode" codeListValue="utf8" codeSpace="ISOTC211/19115">utf8</gmd:MD_CharacterSetCode>
  </gmd:characterSet>
  <gmd:parentIdentifier>
    <gco:CharacterString></gco:CharacterString>
  </gmd:parentIdentifier>
  <gmd:hierarchyLevel>
    <gmd:MD_ScopeCode codeList="http://www.isotc211.org/2005/resources/Codelist/gmxCodelists.xml#MD_ScopeCode" codeListValue="dataset" codeSpace="ISOTC211/19115">dataset</gmd:MD_ScopeCode>
  </gmd:hierarchyLevel>
  <gmd:hierarchyLevelName>
    <gco:CharacterString>dataset</gco:CharacterString>
  </gmd:hierarchyLevelName>
```
::::info
**Contoh Pengisian:**
::::
1. Ganti **[IDENTIFIER_UNIK_DATASET]** menjadi **peta_adm_kab_aceh_2023**

# 2. Kontak Penanggung Jawab
(Ubah dengan data PIC, bisa duplikat blok ini untuk multiple contacts)
### 2.1 Walidata

```xml=
<gmd:contact>
    <gmd:CI_ResponsibleParty>
      <gmd:individualName>
        <gco:CharacterString>[NAMA_LENGKAP_PENANGGUNG_JAWAB_WALIDATA]</gco:CharacterString>
      </gmd:individualName>
      <gmd:organisationName>
        <gco:CharacterString>[NAMA_INSTANSI_WALIDATA]</gco:CharacterString>
      </gmd:organisationName>
      <gmd:positionName>
        <gco:CharacterString>[JABATAN_PENANGGUNG_JAWAB_WALIDATA]</gco:CharacterString>
      </gmd:positionName>
      <gmd:contactInfo>
        <gmd:CI_Contact>
          <gmd:phone>
            <gmd:CI_Telephone>
              <gmd:voice>
                <gco:CharacterString>[NOMOR_TELEPON_WALIDATA]</gco:CharacterString>
              </gmd:voice>
              <gmd:facsimile>
                <gco:CharacterString>[NOMOR_FAX_WALIDATA]</gco:CharacterString>
              </gmd:facsimile>
            </gmd:CI_Telephone>
          </gmd:phone>
          <gmd:address>
            <gmd:CI_Address>
              <gmd:deliveryPoint>
                <gco:CharacterString>[ALAMAT_INSTANSI_WALIDATA]</gco:CharacterString>
              </gmd:deliveryPoint>
              <gmd:city>
                <gco:CharacterString>[NAMA_KABUPATEN/KOTA_WALIDATA]</gco:CharacterString>
              </gmd:city>
              <gmd:administrativeArea>
                <gco:CharacterString>[NAMA_PROVINSI_WALIDATA]</gco:CharacterString>
              </gmd:administrativeArea>
              <gmd:postalCode>
                <gco:CharacterString>[KODEPOS_WALIDATA]</gco:CharacterString>
              </gmd:postalCode>
              <gmd:country>
                <gco:CharacterString>Indonesia</gco:CharacterString>
              </gmd:country>
              <gmd:electronicMailAddress>
                <gco:CharacterString>[EMAIL_RESMI_WALIDATA]</gco:CharacterString>
              </gmd:electronicMailAddress>
            </gmd:CI_Address>
          </gmd:address>
          <gmd:hoursOfService>
            <gco:CharacterString>07.30-16.00</gco:CharacterString>
          </gmd:hoursOfService>
          <gmd:contactInstructions>
            <gco:CharacterString>Hubungi saat jam kerja</gco:CharacterString>
          </gmd:contactInstructions>
        </gmd:CI_Contact>
      </gmd:contactInfo>
      <gmd:role>
        <gmd:CI_RoleCode codeList="./resources/codeList.xml#CI_RoleCode" codeListValue="Walidata">Walidata</gmd:CI_RoleCode>
      </gmd:role>
    </gmd:CI_ResponsibleParty>
  </gmd:contact>
```
::::info
**Contoh Pengisian:**
::::
1. Ganti **[NAMA_LENGKAP_PENANGGUNG_JAWAB_WALIDATA]** menjadi **Dr. Ahmad Setiawan, S.T., M.T**.
2. Ganti **[NAMA_INSTANSI_WALIDATA]** menjadi **Dinas PUPR Provinsi Jawa Barat**
3. Ganti **[JABATAN_PENANGGUNG_JAWAB_WALIDATA]** menjadi **Kepala Bidang Geospasial**
4. Ganti **[NOMOR_TELEPON]** menjadi **021-1234567**
5. Ganti **[NOMOR_FAX]** sesuai dengan nomor fax instansi
6. Ganti **[ALAMAT_INSTANSI_WALIDATA]** dengan alamat lengkap instansi, misalnya: **Jl. Asia Afrika No. 123**
7. Ganti **[NAMA_KABUPATEN/KOTA]** menjadi nama kabupaten/kota, misalnya: **Kota Bandung**
8. Ganti **[NAMA_PROVINSI]** menjadi **Jawa Barat**
9. Ganti **[KODEPOS]** menjadi **40111**
10. Ganti **[EMAIL_RESMI]** menjadi **geospasial@pupr.jabar.go.id**


### 2.2 Produsen Data

```xml=
<gmd:contact>
    <gmd:CI_ResponsibleParty>
      <gmd:individualName>
        <gco:CharacterString>[NAMA_LENGKAP_PENANGGUNG_JAWAB_PRODUSENDATA]</gco:CharacterString>
      </gmd:individualName>
      <gmd:organisationName>
        <gco:CharacterString>[NAMA_INSTANSI_PRODUSENDATA]</gco:CharacterString>
      </gmd:organisationName>
      <gmd:positionName>
        <gco:CharacterString>[JABATAN_PENANGGUNG_JAWAB_PRODUSENDATA]</gco:CharacterString>
      </gmd:positionName>
      <gmd:contactInfo>
        <gmd:CI_Contact>
          <gmd:phone>
            <gmd:CI_Telephone>
              <gmd:voice>
                <gco:CharacterString>[NOMOR_TELEPON_PRODUSENDATA]</gco:CharacterString>
              </gmd:voice>
            </gmd:CI_Telephone>
          </gmd:phone>
          <gmd:address>
            <gmd:CI_Address>
              <gmd:deliveryPoint>
                <gco:CharacterString>[ALAMAT_INSTANSI_PRODUSENDATA]</gco:CharacterString>
              </gmd:deliveryPoint>
              <gmd:city>
                <gco:CharacterString>[NAMA_KABUPATEN/KOTA_PRODUSENDATA]</gco:CharacterString>
              </gmd:city>
              <gmd:administrativeArea>
                <gco:CharacterString>[NAMA_PROVINSI_PRODUSENDATA]</gco:CharacterString>
              </gmd:administrativeArea>
              <gmd:postalCode>
                <gco:CharacterString>[KODEPOS_PRODUSENDATA]</gco:CharacterString>
              </gmd:postalCode>
              <gmd:country>
                <gco:CharacterString>Indonesia</gco:CharacterString>
              </gmd:country>
              <gmd:electronicMailAddress>
                <gco:CharacterString>[EMAIL_RESMI_PRODUSENDATA]</gco:CharacterString>
              </gmd:electronicMailAddress>
            </gmd:CI_Address>
          </gmd:address>
          <gmd:hoursOfService>
            <gco:CharacterString>07.30-16.00</gco:CharacterString>
          </gmd:hoursOfService>
          <gmd:contactInstructions>
            <gco:CharacterString>Hubungi saat jam kerja dan hari kerja</gco:CharacterString>
          </gmd:contactInstructions>
        </gmd:CI_Contact>
      </gmd:contactInfo>
      <gmd:role>
        <gmd:CI_RoleCode codeList="./resources/codeList.xml#CI_RoleCode" codeListValue="Produsen Data">Produsen Data</gmd:CI_RoleCode>
      </gmd:role>
    </gmd:CI_ResponsibleParty>
  </gmd:contact>
```
::::info
**Contoh Pengisian:**
::::
1. Ganti **[NAMA_LENGKAP_PENANGGUNG_JAWAB_PRODUSENDATA]** menjadi **Ir. Budi Santoso, M.Eng.**
2. Ganti **[NAMA_INSTANSI_PRODUSENDATA]** menjadi **Dinas Bina Marga Provinsi Jawa Tengah**
3. Ganti **[JABATAN_PENANGGUNG_JAWAB_PRODUSENDATA]** menjadi **Kepala Seksi Data Jalan dan Jembatan**
4. Ganti **[NOMOR_TELEPON_PRODUSENDATA]** menjadi **024-9876543**
5. Ganti **[ALAMAT_INSTANSI_PRODUSENDATA]** dengan alamat lengkap instansi, misalnya: **Jl. Pemuda No. 45**
6. Ganti **[NAMA_KABUPATEN/KOTA]** menjadi nama kabupaten/kota, misalnya: **Kota Semarang**
7. Ganti **[NAMA_PROVINSI]** menjadi **Jawa Tengah**
8. Ganti **[KODEPOS]** menjadi **50139**
9. Ganti **[EMAIL_RESMI]** menjadi **datamarga@jatengprov.go.id**


# 3. Identifikasi Dataset

```xml=
<gmd:identificationInfo>
    <gmd:MD_DataIdentification>
      <gmd:citation>
        <gmd:CI_Citation>
          <gmd:title>
            <gco:CharacterString>[IDENTIFIER_UNIK_DATASET]</gco:CharacterString>
          </gmd:title>
          <gmd:date>
            <gmd:CI_Date>
              <gmd:date>
                <gco:Date>2025-01-01</gco:Date>
              </gmd:date>
              <gmd:dateType>
                <gmd:CI_DateTypeCode codeList="./resources/codeList.xml#CI_DateTypeCode" codeListValue="publication">publication</gmd:CI_DateTypeCode>
              </gmd:dateType>
            </gmd:CI_Date>
          </gmd:date>
        </gmd:CI_Citation>
      </gmd:citation>
      <gmd:abstract>
        <gco:CharacterString>Data spasial yang di produksi oleh [NAMA_INSTANSI_PRODUSENDATA]</gco:CharacterString>
      </gmd:abstract>
      <gmd:purpose>
        <gco:CharacterString>Diperuntukan hanya untuk Aplikasi Web Geoportal</gco:CharacterString>
      </gmd:purpose>
      <gmd:credit>
        <gco:CharacterString>[NAMA_PROVINSI/KABUPATEN/KOTA]</gco:CharacterString>
      </gmd:credit>
```
::::info
**Contoh Pengisian:**
::::
1. Informasi Dasar: **[IDENTIFIER_UNIK_DATASET]**: Judul lengkap dataset tidak boleh berbeda dari awal paling atas (contoh: "peta_adm_kab_aceh_2023")
2. **[NAMA_INSTANSI_PRODUSEN]**: Nama instansi pembuat data
3. **[NAMA_PROVINSI/KABUPATEN/KOTA]**: Wilayah cakupan data

### 3.1 Point Kontak Produsen Data
```xml=
      <gmd:pointOfContact>
        <gmd:CI_ResponsibleParty>
          <gmd:individualName>
            <gco:CharacterString>[NAMA_LENGKAP_PENANGGUNG_JAWAB_PRODUSENDATA]</gco:CharacterString>
          </gmd:individualName>
          <gmd:organisationName>
            <gco:CharacterString>[NAMA_INSTANSI_PRODUSENDATA]</gco:CharacterString>
          </gmd:organisationName>
          <gmd:positionName>
            <gco:CharacterString>[JABATAN_PENANGGUNG_JAWAB_PRODUSENDATA]</gco:CharacterString>
          </gmd:positionName>
          <gmd:contactInfo>
            <gmd:CI_Contact>
              <gmd:phone>
                <gmd:CI_Telephone>
                  <gmd:voice>
                    <gco:CharacterString>[NOMOR_TELEPON_PRODUSENDATA]</gco:CharacterString>
                  </gmd:voice>
                </gmd:CI_Telephone>
              </gmd:phone>
              <gmd:address>
                <gmd:CI_Address>
                  <gmd:deliveryPoint>
                    <gco:CharacterString>[ALAMAT_INSTANSI_PRODUSENDATA]</gco:CharacterString>
                  </gmd:deliveryPoint>
                  <gmd:city>
                    <gco:CharacterString>[NAMA_KABUPATEN/KOTA_PRODUSENDATA]</gco:CharacterString>
                  </gmd:city>
                  <gmd:administrativeArea>
                    <gco:CharacterString>[NAMA_PROVINSI_PRODUSENDATA]</gco:CharacterString>
                  </gmd:administrativeArea>
                  <gmd:postalCode>
                    <gco:CharacterString>[KODEPOS_PRODUSENDATA]</gco:CharacterString>
                  </gmd:postalCode>
                  <gmd:country>
                    <gco:CharacterString>Indonesia</gco:CharacterString>
                  </gmd:country>
                  <gmd:electronicMailAddress>
                    <gco:CharacterString>[EMAIL_RESMI_PRODUSENDATA]</gco:CharacterString>
                  </gmd:electronicMailAddress>
                </gmd:CI_Address>
              </gmd:address>
              <gmd:hoursOfService>
                <gco:CharacterString>07.30-16.00</gco:CharacterString>
              </gmd:hoursOfService>
              <gmd:contactInstructions>
                <gco:CharacterString>Hubungi saat jam kerja dan hari kerja</gco:CharacterString>
              </gmd:contactInstructions>
            </gmd:CI_Contact>
          </gmd:contactInfo>
          <gmd:role>
            <gmd:CI_RoleCode codeList="./resources/codeList.xml#CI_RoleCode" codeListValue="Produsen Data">Produsen Data</gmd:CI_RoleCode>
          </gmd:role>
        </gmd:CI_ResponsibleParty>
      </gmd:pointOfContact>
```
::::info
**Pengisian Point Kontak Produsen Data:**
::::
1. **[NAMA_LENGKAP_PENANGGUNG_JAWAB_PRODUSENDATA]**: Nama penanggung jawab.
2. **[NAMA_INSTANSI_PRODUSENDATA]**: Nama Instansi produsen data.
3. **[JABATAN_PENANGGUNG_JAWAB_PRODUSENDATA]**: Jabatan penanggung jawab.
4. **[NOMOR_TELEPON_PRODUSENDATA]**: Nomor telepon produsen data.
5. **[ALAMAT_INSTANSI_PRODUSENDATA]**: Alamat lengkap.
6. **[NAMA_KABUPATEN/KOTA]**: Kabupaten/Kota produsen data.
7. **[NOMOR_TELEPON_PRODUSENDATA]**: Nomor telepon aktif instansi/produsen data.
8. **[ALAMAT_INSTANSI_PRODUSENDATA]**: Alamat lengkap instansi produsen data.
9. **[NAMA_PROVINSI]**: Nama Provinsi produsen data.
10. **[KODEPOS]**: Kode pos produsen data.
11. **[EMAIL_RESMI]**: Alamat email resmi instansi atau kontak.

### 3.2 Point Kontak Walidata
```xml=
      <gmd:pointOfContact>
        <gmd:CI_ResponsibleParty>
          <gmd:individualName>
            <gco:CharacterString>[NAMA_LENGKAP_PIC_WALIDATA]</gco:CharacterString>
          </gmd:individualName>
          <gmd:organisationName>
            <gco:CharacterString>[NAMA_INSTANSI_WALIDATA]</gco:CharacterString>
          </gmd:organisationName>
          <gmd:positionName>
            <gco:CharacterString>[JABATAN_PENANGGUNG_JAWAB_WALIDATA]</gco:CharacterString>
          </gmd:positionName>
          <gmd:contactInfo>
            <gmd:CI_Contact>
              <gmd:phone>
                <gmd:CI_Telephone>
                  <gmd:voice>
                    <gco:CharacterString>[NOMOR_TELEPON_WALIDATA]</gco:CharacterString>
                  </gmd:voice>
                  <gmd:facsimile>
                    <gco:CharacterString>[NOMOR_FAX_WALIDATA]</gco:CharacterString>
                  </gmd:facsimile>
                </gmd:CI_Telephone>
              </gmd:phone>
              <gmd:address>
                <gmd:CI_Address>
                  <gmd:deliveryPoint>
                    <gco:CharacterString>[ALAMAT_INSTANSI_WALIDATA]</gco:CharacterString>
                  </gmd:deliveryPoint>
                  <gmd:city>
                    <gco:CharacterString>[NAMA_KABUPATEN/KOTA_WALIDATA]</gco:CharacterString>
                  </gmd:city>
                  <gmd:administrativeArea>
                    <gco:CharacterString>[NAMA_PROVINSI_WALIDATA]</gco:CharacterString>
                  </gmd:administrativeArea>
                  <gmd:postalCode>
                    <gco:CharacterString>[KODEPOS_WALIDATA]</gco:CharacterString>
                  </gmd:postalCode>
                  <gmd:country>
                    <gco:CharacterString>Indonesia</gco:CharacterString>
                  </gmd:country>
                  <gmd:electronicMailAddress>
                    <gco:CharacterString>[EMAIL_RESMI_WALIDATA]</gco:CharacterString>
                  </gmd:electronicMailAddress>
                </gmd:CI_Address>
              </gmd:address>
              <gmd:hoursOfService>
                <gco:CharacterString>07.30-16.00</gco:CharacterString>
              </gmd:hoursOfService>
              <gmd:contactInstructions>
                <gco:CharacterString>Hubungi saat jam kerja</gco:CharacterString>
              </gmd:contactInstructions>
            </gmd:CI_Contact>
          </gmd:contactInfo>
          <gmd:role>
            <gmd:CI_RoleCode codeList="./resources/codeList.xml#CI_RoleCode" codeListValue="Walidata">Walidata</gmd:CI_RoleCode>
          </gmd:role>
        </gmd:CI_ResponsibleParty>
      </gmd:pointOfContact>
```
::::info
**Pengisian Point Kontak Walidata:**
::::
1. **[NAMA_LENGKAP_PIC_WALIDATA]**: Nama lengkap PIC (person-in-charge) dari walidata.
2. **[NAMA_INSTANSI_WALIDATA]** Nama instansi walidata.
3. **[JABATAN_PENANGGUNG_JAWAB_WALIDATA]**: Jabatan PIC walidata.
4. **[NOMOR_TELEPON]** dan **[NOMOR_FAX]**: Nomor telepon dan fax kantor walidata.
5. **[ALAMAT_INSTANSI]**: Alamat lengkap kantor walidata.
6. **[NAMA_KABUPATEN/KOTA]**: Nama Kabupaten/Kota walidata
7. **[NAMA_PROVINSI]**: Nama Provinsi walidata.
8. **[KODEPOS]**: Kode pos walidata.
9. **[EMAIL_RESMI]**: Alamat email resmi instansi atau kontak.

### 3.3 Kata Kunci
```xml=
      <gmd:descriptiveKeywords>
        <gmd:MD_Keywords>
          <gmd:keyword>
            <gco:CharacterString>[KEYWORD_DATA]</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>Indonesia</gco:CharacterString>
          </gmd:keyword>
          <gmd:keyword>
            <gco:CharacterString>[KEYWORD_DATA_DESCRIPTION]</gco:CharacterString>
          </gmd:keyword>
          <gmd:type>
            <gmd:MD_KeywordTypeCode codeList="./resources/codeList.xml#MD_KeywordTypeCode" codeListValue="theme">theme</gmd:MD_KeywordTypeCode>
          </gmd:type>
        </gmd:MD_Keywords>
      </gmd:descriptiveKeywords>
```
::::info
Pengisian Elemen Kata Kunci:
::::
1. **[KEYWORD_DATA]**: Kata kunci utama dataset.
Contoh: Tutupan Lahan
2. **[KEYWORD_DATA_DESCRIPTION]**: Kata kunci tambahan yang menjelaskan konteks atau kategori.
Contoh: Lingkungan, Penggunaan Lahan

### 3.4 Informasi Teknis Dataset
```xml=
      <gmd:spatialRepresentationType>
        <gmd:MD_SpatialRepresentationTypeCode codeList="./resources/codeList.xml#MD_SpatialRepresentationTypeCode" codeListValue="vector">vector</gmd:MD_SpatialRepresentationTypeCode>
      </gmd:spatialRepresentationType>
      <gmd:spatialResolution>
        <gmd:MD_Resolution>
          <gmd:equivalentScale>
            <gmd:MD_RepresentativeFraction>
              <gmd:denominator>
                <gco:Integer>250000</gco:Integer>
              </gmd:denominator>
            </gmd:MD_RepresentativeFraction>
          </gmd:equivalentScale>
        </gmd:MD_Resolution>
      </gmd:spatialResolution>
      <gmd:language>
        <gco:CharacterString>Indonesia</gco:CharacterString>
      </gmd:language>
      <gmd:characterSet gco:nilReason="missing"></gmd:characterSet>
      <gmd:topicCategory gco:nilReason="missing"></gmd:topicCategory>
      <gmd:extent>
        <gmd:EX_Extent>
          <gmd:description gco:nilReason="missing"></gmd:description>
          <gmd:geographicElement>
            <gmd:EX_GeographicBoundingBox>
              <gmd:extentTypeCode>
                <gco:Boolean>true</gco:Boolean>
              </gmd:extentTypeCode>
              <gmd:westBoundLongitude>
                <gco:Decimal>94.76832054500005</gco:Decimal>
              </gmd:westBoundLongitude>
              <gmd:eastBoundLongitude>
                <gco:Decimal>141.00007415200002</gco:Decimal>
              </gmd:eastBoundLongitude>
              <gmd:southBoundLatitude>
                <gco:Decimal>-11.007615089999945</gco:Decimal>
              </gmd:southBoundLatitude>
              <gmd:northBoundLatitude>
                <gco:Decimal>8.625482053000042</gco:Decimal>
              </gmd:northBoundLatitude>
            </gmd:EX_GeographicBoundingBox>
          </gmd:geographicElement>
          <gmd:temporalElement gco:nilReason="missing"></gmd:temporalElement>
          <gmd:verticalElement gco:nilReason="missing"></gmd:verticalElement>
        </gmd:EX_Extent>
      </gmd:extent>
      <gmd:supplementalInformation>
        <gco:CharacterString>[ABSTRACT]</gco:CharacterString>
      </gmd:supplementalInformation>
    </gmd:MD_DataIdentification>
  </gmd:identificationInfo>
```
::::info
Pengisian Informasi Teknis Dataset:
::::
1. Tidak banyak perubahan pada bagian ini, hanya penyesuaian saja dengan metadata yang dipunya
2. **[ABSTRACT]**: Deskripsi tambahan dataset. Dapat diisi dengan narasi singkat:
Contoh: Dataset ini berisi data vektor tutupan lahan untuk keperluan perencanaan wilayah.

# 4. Distribusi Data
```XML=
<gmd:distributionInfo>
    <gmd:MD_Distribution>
      <gmd:distributionFormat gco:nilReason="missing"></gmd:distributionFormat>
      <gmd:transferOptions>
        <gmd:MD_DigitalTransferOptions>
          <gmd:unitsOfDistribution>
            <gco:CharacterString>Layers</gco:CharacterString>
          </gmd:unitsOfDistribution>
          <gmd:onLine>
            <gmd:CI_OnlineResource>
              <gmd:linkage>
                <gmd:URL>[URL_NAMA_DOMAIN]/geoserver/palapa/wms</gmd:URL>
              </gmd:linkage>
              <gmd:protocol>
                <gco:CharacterString>OGC:WMS</gco:CharacterString>
              </gmd:protocol>
              <gmd:name>
                <gco:CharacterString>palapa:[IDENTIFIER_UNIK_DATASET]</gco:CharacterString>
              </gmd:name>
            </gmd:CI_OnlineResource>
          </gmd:onLine>
        </gmd:MD_DigitalTransferOptions>
      </gmd:transferOptions>
    </gmd:MD_Distribution>
  </gmd:distributionInfo>
```
::::info
**Contoh Pengisian:**
::::
1. **[URL_NAMA_DOMAIN]**: Masukkan URL domain tempat layanan geoserver Anda tersedia. Contoh: **http://geoportal.purbalinggakab.go.id**
2. Pastikan **[IDENTIFIER_UNIK_DATASET]** konsisten dengan yang diisi sebelumnya (**peta_adm_kab_aceh_2023**)

# 5. Upload Metadata
<div style="text-align: justify;">Berikut langkah-langkah untuk melakukan unggah (upload) metadata XML dan publikasi melalui dashboard walidata di Geoportal Palapa 5.0:

**1. Masuk ke Dashboard Walidata**
Akses menu dashboard walidata dengan akun yang telah diberikan hak akses.

**2. Navigasi ke Menu "Publikasi CSW"**
Pada sidebar menu, klik "Publikasi CSW" untuk melihat daftar metadata yang tersedia.

**3. Pilih Metadata yang Akan Dipublikasikan**
Cari metadata yang sudah siap untuk dipublikasikan, kemudian klik ikon globe 🌐 pada baris metadata tersebut.

**4.Form Penyesuaian Metadata**
Setelah ikon globe diklik, akan muncul form penyesuaian metadata. Di sinilah metadata XML akan disesuaikan sebelum dipublikasikan.
::::info
![image](https://hackmd.io/_uploads/HkpReTryxl.png)
<div style="text-align: center;">Tampilan Publish CSW</div>
::::
**5. Klik Tombol "Upload New XML"**
Klik tombol "Upload New XML" untuk mengunggah file metadata berformat .xml. Pilih file dari perangkat Anda yang sudah dilakukan pengisian sebelumnya.

**6. Tinjau Metadata XML yang Telah Diunggah**
Metadata XML yang berhasil diunggah akan ditampilkan dalam form. Periksa kembali seluruh informasi untuk memastikan kesesuaian dengan standar dan isian yang benar.

**7. Klik "Publish Metadata"**
Jika semua informasi sudah sesuai, klik tombol "Publish Metadata" untuk mempublikasikan metadata ke dalam layanan CSW.
::::info
![image](https://hackmd.io/_uploads/HkDTV6S1xe.png)
<div style="text-align: center;">List Data Terpublish</div>
::::
