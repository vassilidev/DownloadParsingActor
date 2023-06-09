# Project Title

Download a file and parse it to output format easly in Apify from actor to task

## Usage/Examples

```javascript
const dataToSend = {
    "url": "https://www.orimi.com/pdf-test.pdf",
    "outputFormat": "txt"
};

const data = await $.ajax({
    url: "https://api.apify.com/v2/acts/commoprices~downloadparsing/run-sync?token=<TOKEN>",
    method: "POST",
    timeout: 0,
    contentType: "application/json; charset=utf-8",
    data: JSON.stringify(dataToSend)
});

console.dir(data)
```

## API Reference

#### Required parameters

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `url` | `string` | **The url of your file to download** |
| `outputFormat` | `string` | **Output Format of your input file** *(Check for valid pairs)* |

#### Avaible Pairs

| Input        | Output |
|:-------------|:-------|
| `png` `jpg` `jpeg` | `txt`  |
| `xlsx` `xls` | `txt`  |
| `xlsx` `xls` | `csv`  |
| `xlsx` `xls` | `json` |
| `html` `htm` | `txt`  |
| `pdf`        | `txt`  |
| `docx`       | `txt`  |

## Used By

This project is used by the following companies:

- CommoPrices
- Réussir

## Roadmap

- Additional pairs support

- Add more integrations

- Add more documentation

- Add wiki page

## Authors

[@vassilidev](https://github.com/vassilidev) & [@BenjaminG95](https://github.com/BenjaminG95)

## Support

For support, create an issue or email us at vassili.joffroy@commoprices.com / benjamin.galois@commoprices.com

