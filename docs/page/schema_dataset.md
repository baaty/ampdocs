---
layout: page
---

### 説明

データセットの名前、説明、作成者、配布形式など

### タイプ

| タイプ名 | 説明         |
| -------- | ------------ |
| Dataset  | データセット |

### プロパティ

| プロパティ名      | 説明                               |
| ----------------- | ---------------------------------- |
| description(必須) | データセットの要約文               |
| name(必須)        | データセットのわかりやすい名前     |
| alternateName     | エイリアスや略語など               |
| creator           | データセットの作成者               |
| citation          | 引用されている記事                 |
| identifier        | DOIやコンパクト識別子などの識別子 |
| keywords          | データセットの概要を示すキーワード |
| license           | データセットの配布ライセンス       |
| sameAs            | データセットのURL                 |
| spatialCoverage   | データセットの空間様相             |
| temporalCoverage  | 期間                               |
| variableMeasured  | データセットが測定する変数         |
| version           | バージョン                         |
| url               | URL                                |

### 例

    <script type="application/ld+json">
    {
      "@context":"https://schema.org/",
      "@type":"Dataset",
      "name":"NCDC Storm Events Database",
      "description":"Storm Data is provided by the National Weather Service (NWS) and contain statistics on...",
      "url":"https://catalog.data.gov/dataset/ncdc-storm-events-database",
      "sameAs":"https://gis.ncdc.noaa.gov/geoportal/catalog/search/resource/details.page?id=gov.noaa.ncdc:C00510",
      "identifier": ["https://doi.org/10.1000/182",
                     "https://identifiers.org/ark:/12345/fk1234"],
      "keywords":[
         "ATMOSPHERE > ATMOSPHERIC PHENOMENA > CYCLONES",
         "ATMOSPHERE > ATMOSPHERIC PHENOMENA > DROUGHT",
         "ATMOSPHERE > ATMOSPHERIC PHENOMENA > FOG",
         "ATMOSPHERE > ATMOSPHERIC PHENOMENA > FREEZE"
      ],
      "license" : "https://creativecommons.org/publicdomain/zero/1.0/",
      "hasPart" : [
        {
          "@type": "Dataset",
          "name": "Sub dataset 01",
          "description": "Informative description of the first subdataset...",
          "license" : "https://creativecommons.org/publicdomain/zero/1.0/"
        },
        {
          "@type": "Dataset",
          "name": "Sub dataset 02",
          "description": "Informative description of the second subdataset...",
          "license" : "https://creativecommons.org/publicdomain/zero/1.0/"
        }
      ],
      "creator":{
         "@type":"Organization",
         "url": "https://www.ncei.noaa.gov/",
         "name":"OC/NOAA/NESDIS/NCEI > National Centers for Environmental Information, NESDIS, NOAA, U.S. Department of Commerce",
         "contactPoint":{
            "@type":"ContactPoint",
            "contactType": "customer service",
            "telephone":"+1-828-271-4800",
            "email":"ncei.orders@noaa.gov"
         }
      },
      "includedInDataCatalog":{
         "@type":"DataCatalog",
         "name":"data.gov"
      },
      "distribution":[
         {
            "@type":"DataDownload",
            "encodingFormat":"CSV",
            "contentUrl":"http://www.ncdc.noaa.gov/stormevents/ftp.jsp"
         },
         {
            "@type":"DataDownload",
            "encodingFormat":"XML",
            "contentUrl":"http://gis.ncdc.noaa.gov/all-records/catalog/search/resource/details.page?id=gov.noaa.ncdc:C00510"
         }
      ],
      "temporalCoverage":"1950-01-01/2013-12-18",
      "spatialCoverage":{
         "@type":"Place",
         "geo":{
            "@type":"GeoShape",
            "box":"18.0 -65.0 72.0 172.0"
         }
      }
    }
    </script>
