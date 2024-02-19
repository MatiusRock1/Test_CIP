---


---

<h1 id="cip-workflow-webhook-example">CIP workflow webhook example</h1>

Variables para callback messages.opcionales, para uso de mensajes para el usuario, tanto en exito como en error

"callbackUrl" : "www.google.com",

"callbackUrlText" : "this is a callback url ok",

"callbackUrlError": "www.google.com/error",

"callBackUrlTextError" : "this is a callback url error",

<p>Cases</p>

<table>
<thead>
<tr>
<th>Pams/Cases</th>
<th>1</th>
<th>2</th>
<th>3</th>
<th>4</th>
<th>5</th>
<th>6</th>
<th>7</th>
</tr>
</thead>
<tbody>
<tr>
<td>proofOfLife</td>
<td>True</td>
<td>True</td>
<td>True</td>
<td>False</td>
<td>False</td>
<td>False</td>
<td>False</td>
</tr>
<tr>
<td>requestId</td>
<td>False</td>
<td>False</td>
<td>True</td>
<td>True</td>
<td>True</td>
<td>True</td>
<td>False</td>
</tr>
<tr>
<td>requestSelfie</td>
<td>False</td>
<td>False</td>
<td>False</td>
<td>True</td>
<td>False</td>
<td>False</td>
<td>True</td>
</tr>
<tr>
<td>validateIdName</td>
<td>False</td>
<td>False</td>
<td>T/F</td>
<td>T/F</td>
<td>T/f</td>
<td>T/F</td>
<td>False</td>
</tr>
<tr>
<td>referenceImage</td>
<td>Exist</td>
<td>None</td>
<td>Ignore</td>
<td>Ignore</td>
<td>Exist</td>
<td>None</td>
<td>Exist</td>
</tr>
</tbody>
</table><h2 id="case-1">Case 1</h2>
<p>Request in service token/create</p>
<pre><code>    {
        "userId": "+123235451234567892",
        "firstName": "JELANI",
        "lastName": "SAMPLE",
        "proofOfLife": true,
        "requestId": false,
        "requestSelfie" : false,
        "validateIdName": false,
        ,    
		"webhookUrl":"https://webhook.site/db0497cf-c4e3-48f0-9637-8d3618be6285",
        "referenceImage": "https://www.sarasa.com/sarasa.png",
        "targetCountry": "US",
        "ttlInSeconds": 360000,
        "allowedPlatforms": ["telegram", "whatsapp", "sms", "webchat"],
        "brandName": "Hway",
        "theme": {
	        "fullLogoUrl": "https://www.sarasa.com/sarasa.png",
	        "primaryColor": "#000000",
	        "secondaryColor": "#000000",
	        "thirdColor": "#000000",
	        "surfaceColor": "#000000"
        }    
    }
</code></pre>
<p>Webhook in finish process:</p>
<pre><code>{
      "cipToken": {
        "userId": "+123235451234567892",
        "firstName": "JELANI",
        "lastName": "SAMPLE",
        "proofOfLife": true,
        "requestId": false,
        "requestSelfie": false,
        "validateIdName": false,
        "referenceImage": "https://firebasestorage.googleapis.com/v0/b/numichat.appspot.com/o/test_images%2Freference_image%2FImagen%20de%20WhatsApp%202023-05-25%20a%20las%2009.50.58.jpg?alt=media&amp;token=8c2e5682-b0f6-44b7-b1e5-ef8f212be19f",
        "targetCountry": "US",
        "ttlInSeconds": 360000,
        "allowedPlatforms": [
          "telegram",
          "whatsapp",
          "sms",
          "webchat"
        ],
        "brandName": "Hway",
        "theme": {
          "fullLogoUrl": "https://www.sarasa.com/sarasa.png",
          "primaryColor": "#000000",
          "secondaryColor": "#000000",
          "thirdColor": "#000000",
          "surfaceColor": "#000000"
        },
        "id": "u9CeCjAzjzUbexmTtivLcU",
        "allowedCountriesIds": [
          
        ],
        "language": "en",
        "validateExpDate": false,
        "claimed": true,
        "claimedAt": "2023-05-29T16:45:37.493Z",
        "claimedBy": "e19v5NZmrfUURo3XohBBgp",
        "claimedPlatformId": "chatwoot"
      },
      "last_frame": "Base64",
      "selfie_img_check": true,
      "pol_check": true,
      "face_match": {
        "status": "success",
        "message": "Success",
        "identical": true,
        "confidence": 0.7449953459214909
      }
    }
</code></pre>
<h2 id="case-2">Case 2</h2>
<p>Request in service token/create</p>
<pre><code> {
      "userId": "+123235451234567892",
      "firstName": "JELANI",
      "lastName": "SAMPLE",
      "proofOfLife": true,
      "requestId": false,
      "requestSelfie": false,
      "validateIdName": false,
      ,
"webhookUrl":"https://webhook.site/db0497cf-c4e3-48f0-9637-8d3618be6285",
      "targetCountry": "US",
      "ttlInSeconds": 360000,
      "allowedPlatforms": [
        "telegram",
        "whatsapp",
        "sms",
        "webchat"
      ],
      "brandName": "Hway",
      "theme": {
        "fullLogoUrl": "https://www.sarasa.com/sarasa.png",
        "primaryColor": "#000000",
        "secondaryColor": "#000000",
        "thirdColor": "#000000",
        "surfaceColor": "#000000"
      }
    }
</code></pre>
<p>Webhook in finish process:</p>
<pre><code>{
  "cipToken": {
    "userId": "+123235451234567893",
    "firstName": "JELANI",
    "lastName": "SAMPLE",
    "proofOfLife": true,
    "requestId": false,
    "requestSelfie": false,
    "validateIdName": false,
    "targetCountry": "US",
    "ttlInSeconds": 360000,
    "allowedPlatforms": [
      "telegram",
      "whatsapp",
      "sms",
      "webchat"
    ],
    "brandName": "Hway",
    "theme": {
      "fullLogoUrl": "https://www.sarasa.com/sarasa.png",
      "primaryColor": "#000000",
      "secondaryColor": "#000000",
      "thirdColor": "#000000",
      "surfaceColor": "#000000"
    },
    "id": "cac1VQtyGYnZCujcHwaP6J",
    "allowedCountriesIds": [
      
    ],
    "language": "en",
    "validateExpDate": false,
    "claimed": true,
    "claimedAt": "2023-05-29T16:58:49.611Z",
    "claimedBy": "e19v5NZmrfUURo3XohBBgp",
    "claimedPlatformId": "chatwoot"
  },
  "last_frame": "Base64",      
}
</code></pre>
<h2 id="case-3">Case 3</h2>
<p>Request in service token/create</p>
<pre><code>{
  "userId": "+123235451234567896",
  "firstName": "JELANI",
  "lastName": "SAMPLE",
  "proofOfLife": true,
  "requestId": true,
  "requestSelfie": false,
  "validateIdName": true,
  ,
"webhookUrl":"https://webhook.site/db0497cf-c4e3-48f0-9637-8d3618be6285",
  "targetCountry": "US",
  "ttlInSeconds": 360000,
  "allowedPlatforms": [
    "telegram",
    "whatsapp",
    "sms",
    "webchat"
  ],
  "brandName": "Hway",
  "theme": {
    "fullLogoUrl": "https://www.sarasa.com/sarasa.png",
    "primaryColor": "#000000",
    "secondaryColor": "#000000",
    "thirdColor": "#000000",
    "surfaceColor": "#000000"
  }
}
</code></pre>
<p>Webhook in finish process:</p>
<pre><code>  {
      "cipToken": {
        "userId": "+123235451234567896",
        "firstName": "JELANI",
        "lastName": "SAMPLE",
        "proofOfLife": true,
        "requestId": true,
        "requestSelfie": false,
        "validateIdName": true,
        "targetCountry": "US",
        "ttlInSeconds": 360000,
        "allowedPlatforms": [
          "telegram",
          "whatsapp",
          "sms",
          "webchat"
        ],
        "brandName": "Hway",
        "theme": {
          "fullLogoUrl": "https://www.sarasa.com/sarasa.png",
          "primaryColor": "#000000",
          "secondaryColor": "#000000",
          "thirdColor": "#000000",
          "surfaceColor": "#000000"
        },
        "id": "rVkMKJyLQp58W6y2LBs4PE",
        "allowedCountriesIds": [
          
        ],
        "language": "en",
        "validateExpDate": false,
        "claimed": true,
        "claimedAt": "2023-05-29T17:32:59.104Z",
        "claimedBy": "p13XRnohuv1V8WCkfxtYxi",
        "claimedPlatformId": "chatwoot"
      },
      "validateIdName": {
"isMatched": true,
"score": 0.8571428571428572,
"matchNameResults": {
  "success": true,
  "averageScore": 0.8571428571428572,
  "matches": [
    {
      "key": "firstName",
      "match": {
        "item": "JELANI",
        "original": "JELANI",
        "key": "jelani",
        "score": 0.7142857142857143,
        "match": {
          "index": 0,
          "length": 5
        }
      }
    },
    {
      "key": "lastName",
      "match": {
        "item": "SAMPLE",
        "original": "SAMPLE",
        "key": "sample",
        "score": 1,
        "match": {
          "index": 0,
          "length": 6
        }
      }
    }
  ],
  "reason": "Average score is 0.8571428571428572"
}
</code></pre>
<p>},</p>
<pre><code>"dateBirth": "1974-01-01",
      "address": "123 Main St, Phoenix, AZ 85007",
      "ocr_id": {
        "plainText": "Arizona DRIVER LICENSE USA\n9 CLASS D\n9a END NONE\n12 REST B\nSample\nJelaine.\n1 SAMPLE\n2 JELANI\n8 123 MAIN ST\nPHOENIX, AZ 85007\n4d DLN D08954796\n3 DOB 01/01/1974\n4b EXP 03/01/2024 4a ISS 03/01/2016\n294\n18 EYES BRO VETERAN\n01/01/74\n15 SEX M\n16 HGT 5'-09\" 19 HAIR BRO\n17 WGT 185 lb\nDONOR\n5 DD 9001A9691S1421J4\n",
        "data": {
          "DocumentType": "Driver License",
          "Country": "USA",
          "Country2": "US",
          "IDNumber": "D08954796",
          "FullName": "Jelaine Sample",
          "FirstName": "Jelaine",
          "LastName": "Sample",
          "Address": "123 Main St, Phoenix, AZ 85007",
          "Gender": "M",
          "DoB": "1974-01-01",
          "IssueDate": "2016-03-01",
          "ExpDate": "2024-03-01",
          "Eyes": "BRO",
          "Veteran": true,
          "Height": "5'-09\"",
          "Hair": "BRO",
          "Weight": "185 lb",
          "Donor": true,
          "DD": "9001A9691S1421J4"
        }
      },
      "id_img": "https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBOXU0V3c9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--5e83815e90284bea840de6a6f391311a3a498a67/file_2.jpg",
      "id_img_check": true,
      "id_data": "DocumentType: Driver License \nCountry: USA \nCountry2: US \nIDNumber: D08954796 \nFullName: Jelaine Sample \nFirstName: Jelaine \nLastName: Sample \nAddress: 123 Main St, Phoenix, AZ 85007 \nGender: M \nDoB: 1974-01-01 \nIssueDate: 2016-03-01 \nExpDate: 2024-03-01 \nEyes: BRO \nVeteran: true \nHeight: 5'-09\" \nHair: BRO \nWeight: 185 lb \nDonor: true \nDD: 9001A9691S1421J4 \n",
      "face_from_id_b64": "base64",
      "last_frame": "Base64",
      "selfie_img_check": true,
      "pol_check": true,
    }
</code></pre>
<h2 id="case-4">Case 4</h2>
<p>Request in service token/create</p>
<pre><code>{
  "userId": "+123235451234567896",
  "firstName": "JELANI",
  "lastName": "SAMPLE",
  "proofOfLife": false,
  "requestId": true,
  "requestSelfie": true,
  "validateIdName": true,
  ,
"webhookUrl":"https://webhook.site/db0497cf-c4e3-48f0-9637-8d3618be6285",
  "targetCountry": "US",
  "ttlInSeconds": 360000,
  "allowedPlatforms": [
    "telegram",
    "whatsapp",
    "sms",
    "webchat"
  ],
  "brandName": "Hway",
  "theme": {
    "fullLogoUrl": "https://www.sarasa.com/sarasa.png",
    "primaryColor": "#000000",
    "secondaryColor": "#000000",
    "thirdColor": "#000000",
    "surfaceColor": "#000000"
  }
}
</code></pre>
<p>Webhook in finish process:</p>
<pre><code>{
  "cipToken": {
    "userId": "+123235451234567910",
    "firstName": "JELANI",
    "lastName": "SAMPLE",
    "proofOfLife": false,
    "requestId": true,
    "requestSelfie": true,
    "validateIdName": true,
    "targetCountry": "US",
    "ttlInSeconds": 360000,
    "allowedPlatforms": [
      "telegram",
      "whatsapp",
      "sms",
      "webchat"
    ],
    "brandName": "Hway",
    "theme": {
      "fullLogoUrl": "https://www.sarasa.com/sarasa.png",
      "primaryColor": "#000000",
      "secondaryColor": "#000000",
      "thirdColor": "#000000",
      "surfaceColor": "#000000"
    },
    "id": "rK2KSCrVCKeeibusnvSTzu",
    "allowedCountriesIds": [
      
    ],
    "language": "en",
    "validateExpDate": false,
    "claimed": true,
    "claimedAt": "2023-05-29T20:58:05.475Z",
    "claimedBy": "cPusEXJVHqEHpyEALXzQ2C",
    "claimedPlatformId": "chatwoot"
  },
  "validateIdName": {
"isMatched": true,
"score": 0.8571428571428572,
"matchNameResults": {
  "success": true,
  "averageScore": 0.8571428571428572,
  "matches": [
    {
      "key": "firstName",
      "match": {
        "item": "JELANI",
        "original": "JELANI",
        "key": "jelani",
        "score": 0.7142857142857143,
        "match": {
          "index": 0,
          "length": 5
        }
      }
    },
    {
      "key": "lastName",
      "match": {
        "item": "SAMPLE",
        "original": "SAMPLE",
        "key": "sample",
        "score": 1,
        "match": {
          "index": 0,
          "length": 6
        }
      }
    }
  ],
  "reason": "Average score is 0.8571428571428572"
}
 },
      "dateBirth": "1974-01-01",
      "address": "123 Main St, Phoenix, AZ 85007",
      "ocr_id": {
        "plainText": "Arizona DRIVER LICENSE USA\n9 CLASS D\n9a END NONE\n12 REST B\nSample\nJelaine.\n1 SAMPLE\n2 JELANI\n8 123 MAIN ST\nPHOENIX, AZ 85007\n4d DLN D08954796\n3 DOB 01/01/1974\n4b EXP 03/01/2024 4a ISS 03/01/2016\n294\n18 EYES BRO VETERAN\n01/01/74\n15 SEX M\n16 HGT 5'-09\" 19 HAIR BRO\n17 WGT 185 lb\nDONOR\n5 DD 9001A9691S1421J4\n",
        "data": {
          "DocumentType": "Driver License",
          "Country": "USA",
          "Country2": "US",
          "IDNumber": "D08954796",
          "FullName": "Jelaine Sample",
          "FirstName": "Jelaine",
          "LastName": "Sample",
          "Address": "123 Main St, Phoenix, AZ 85007",
          "Gender": "M",
          "DoB": "1974-01-01",
          "IssueDate": "2016-03-01",
          "ExpDate": "2024-03-01",
          "Eyes": "BRO",
          "Veteran": true,
          "Height": "5'-09\"",
          "Hair": "BRO",
          "Weight": "185 lb",
          "Donor": true,
          "DD": "9001A9691S1421J4"
        }
      },
      "id_img": "https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBMGUrV3c9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--9cd5ddd205a5e50adac2e8fa4bde86f922187803/file_2.jpg",
      "id_img_check": true,
      "id_data": "DocumentType: Driver License \nCountry: USA \nCountry2: US \nIDNumber: D08954796 \nFullName: Jelaine Sample \nFirstName: Jelaine \nLastName: Sample \nAddress: 123 Main St, Phoenix, AZ 85007 \nGender: M \nDoB: 1974-01-01 \nIssueDate: 2016-03-01 \nExpDate: 2024-03-01 \nEyes: BRO \nVeteran: true \nHeight: 5'-09\" \nHair: BRO \nWeight: 185 lb \nDonor: true \nDD: 9001A9691S1421J4 \n",
      "face_from_id_b64": "base64",
      "selfie_img_check": true
    }
</code></pre>
<h2 id="case-5">Case 5</h2>
<p>Request in service token/create</p>
<pre><code>{
  "userId": "+123235451234567897",
  "firstName": "JELANI",
  "lastName": "SAMPLE",
  "proofOfLife": false,
  "requestId": true,
  "requestSelfie": false,
  "validateIdName": true,
  ,
"webhookUrl":"https://webhook.site/db0497cf-c4e3-48f0-9637-8d3618be6285",
      "referenceImage": "https://www.sarasa.com/sarasa.png",
      "targetCountry": "US",
      "ttlInSeconds": 360000,
      "allowedPlatforms": [
        "telegram",
        "whatsapp",
        "sms",
        "webchat"
      ],
      "brandName": "Hway",
      "theme": {
        "fullLogoUrl": "https://www.sarasa.com/sarasa.png",
        "primaryColor": "#000000",
        "secondaryColor": "#000000",
        "thirdColor": "#000000",
        "surfaceColor": "#000000"
      }

}
</code></pre>
<p>Webhook in finish process:</p>
<pre><code>{
  "cipToken": {
    "userId": "+123235451234567911",
    "firstName": "JELANI",
    "lastName": "SAMPLE",
    "proofOfLife": false,
    "requestId": true,
    "requestSelfie": false,
    "validateIdName": true,
    "targetCountry": "US",
    "ttlInSeconds": 360000,
    "allowedPlatforms": [
      "telegram",
      "whatsapp",
      "sms",
      "webchat"
    ],
    "brandName": "Hway",
    "theme": {
      "fullLogoUrl": "https://www.sarasa.com/sarasa.png",
      "primaryColor": "#000000",
      "secondaryColor": "#000000",
      "thirdColor": "#000000",
      "surfaceColor": "#000000"
    },
    "id": "c3tKZs4u4sTDZDNtPravRV",
    "allowedCountriesIds": [
      
    ],
    "language": "en",
    "validateExpDate": false,
    "claimed": true,
    "claimedAt": "2023-05-29T21:02:00.926Z",
    "claimedBy": "6ay4XiLPseybMNFcxKi8TZ",
    "claimedPlatformId": "chatwoot"
  },
  "validateIdName": {
"isMatched": true,
"score": 0.8571428571428572,
"matchNameResults": {
  "success": true,
  "averageScore": 0.8571428571428572,
  "matches": [
    {
      "key": "firstName",
      "match": {
        "item": "JELANI",
        "original": "JELANI",
        "key": "jelani",
        "score": 0.7142857142857143,
        "match": {
          "index": 0,
          "length": 5
        }
      }
    },
    {
      "key": "lastName",
      "match": {
        "item": "SAMPLE",
        "original": "SAMPLE",
        "key": "sample",
        "score": 1,
        "match": {
          "index": 0,
          "length": 6
        }
      }
    }
  ],
  "reason": "Average score is 0.8571428571428572"
}


 },
      "dateBirth": "1974-01-01",
      "address": "123 Main St, Phoenix, AZ 85007",
      "ocr_id": {
        "plainText": "Arizona DRIVER LICENSE USA\n9 CLASS D\n9a END NONE\n12 REST B\nSample\nJelaine.\n1 SAMPLE\n2 JELANI\n8 123 MAIN ST\nPHOENIX, AZ 85007\n4d DLN D08954796\n3 DOB 01/01/1974\n4b EXP 03/01/2024 4a ISS 03/01/2016\n294\n18 EYES BRO VETERAN\n01/01/74\n15 SEX M\n16 HGT 5'-09\" 19 HAIR BRO\n17 WGT 185 lb\nDONOR\n5 DD 9001A9691S1421J4\n",
        "data": {
          "DocumentType": "Driver License",
          "Country": "USA",
          "Country2": "US",
          "IDNumber": "D08954796",
          "FullName": "Jelaine Sample",
          "FirstName": "Jelaine",
          "LastName": "Sample",
          "Address": "123 Main St, Phoenix, AZ 85007",
          "Gender": "M",
          "DoB": "1974-01-01",
          "IssueDate": "2016-03-01",
          "ExpDate": "2024-03-01",
          "Eyes": "BRO",
          "Veteran": true,
          "Height": "5'-09\"",
          "Hair": "BRO",
          "Weight": "185 lb",
          "Donor": true,
          "DD": "9001A9691S1421J4"
        }
      },
      "id_img": "https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBMnkrV3c9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--65ced65b87de701e9fcd500e4ec68fbc5c93b1ac/file_2.jpg",
      "id_img_check": true,
      "id_data": "DocumentType: Driver License \nCountry: USA \nCountry2: US \nIDNumber: D08954796 \nFullName: Jelaine Sample \nFirstName: Jelaine \nLastName: Sample \nAddress: 123 Main St, Phoenix, AZ 85007 \nGender: M \nDoB: 1974-01-01 \nIssueDate: 2016-03-01 \nExpDate: 2024-03-01 \nEyes: BRO \nVeteran: true \nHeight: 5'-09\" \nHair: BRO \nWeight: 185 lb \nDonor: true \nDD: 9001A9691S1421J4 \n"
    }
</code></pre>
<h2 id="case-6">Case 6</h2>
<p>Request in service token/create</p>
<pre><code> {
      "userId": "+123235451234567899",
      "firstName": "JELANI",
      "lastName": "SAMPLE",
      "proofOfLife": false,
      "requestId": true,
      "requestSelfie": false,
      "validateIdName": true,
      ,
	  "webhookUrl":"https://webhook.site/db0497cf-c4e3-48f0-9637-8d3618be6285",
      "targetCountry": "US",
      "ttlInSeconds": 360000,
      "allowedPlatforms": [
        "telegram",
        "whatsapp",
        "sms",
        "webchat"
      ],
      "brandName": "Hway",
      "theme": {
        "fullLogoUrl": "https://www.sarasa.com/sarasa.png",
        "primaryColor": "#000000",
        "secondaryColor": "#000000",
        "thirdColor": "#000000",
        "surfaceColor": "#000000"
      }
    }
</code></pre>
<p>Webhook in finish process:</p>
<pre><code>{
  "cipToken": {
    "userId": "+123235451234567911",
    "firstName": "JELANI",
    "lastName": "SAMPLE",
    "proofOfLife": false,
    "requestId": true,
    "requestSelfie": false,
    "validateIdName": true,
    "targetCountry": "US",
    "ttlInSeconds": 360000,
    "allowedPlatforms": [
      "telegram",
      "whatsapp",
      "sms",
      "webchat"
    ],
    "brandName": "Hway",
    "theme": {
      "fullLogoUrl": "https://www.sarasa.com/sarasa.png",
      "primaryColor": "#000000",
      "secondaryColor": "#000000",
      "thirdColor": "#000000",
      "surfaceColor": "#000000"
    },
    "id": "c3tKZs4u4sTDZDNtPravRV",
    "allowedCountriesIds": [
      
    ],
    "language": "en",
    "validateExpDate": false,
    "claimed": true,
    "claimedAt": "2023-05-29T21:02:00.926Z",
    "claimedBy": "6ay4XiLPseybMNFcxKi8TZ",
    "claimedPlatformId": "chatwoot"
  },
  "validateIdName": {
"isMatched": true,
"score": 0.8571428571428572,
"matchNameResults": {
  "success": true,
  "averageScore": 0.8571428571428572,
  "matches": [
    {
      "key": "firstName",
      "match": {
        "item": "JELANI",
        "original": "JELANI",
        "key": "jelani",
        "score": 0.7142857142857143,
        "match": {
          "index": 0,
          "length": 5
        }
      }
    },
    {
      "key": "lastName",
      "match": {
        "item": "SAMPLE",
        "original": "SAMPLE",
        "key": "sample",
        "score": 1,
        "match": {
          "index": 0,
          "length": 6
        }
      }
    }
  ],
  "reason": "Average score is 0.8571428571428572"
}
  },

 "dateBirth": "1974-01-01",
  "address": "123 Main St, Phoenix, AZ 85007",
  "ocr_id": {
    "plainText": "Arizona DRIVER LICENSE USA\n9 CLASS D\n9a END NONE\n12 REST B\nSample\nJelaine.\n1 SAMPLE\n2 JELANI\n8 123 MAIN ST\nPHOENIX, AZ 85007\n4d DLN D08954796\n3 DOB 01/01/1974\n4b EXP 03/01/2024 4a ISS 03/01/2016\n294\n18 EYES BRO VETERAN\n01/01/74\n15 SEX M\n16 HGT 5'-09\" 19 HAIR BRO\n17 WGT 185 lb\nDONOR\n5 DD 9001A9691S1421J4\n",
    "data": {
      "DocumentType": "Driver License",
      "Country": "USA",
      "Country2": "US",
      "IDNumber": "D08954796",
      "FullName": "Jelaine Sample",
      "FirstName": "Jelaine",
      "LastName": "Sample",
      "Address": "123 Main St, Phoenix, AZ 85007",
      "Gender": "M",
      "DoB": "1974-01-01",
      "IssueDate": "2016-03-01",
      "ExpDate": "2024-03-01",
      "Eyes": "BRO",
      "Veteran": true,
      "Height": "5'-09\"",
      "Hair": "BRO",
      "Weight": "185 lb",
      "Donor": true,
      "DD": "9001A9691S1421J4"
    }
  },
  "id_img": "https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBMnkrV3c9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--65ced65b87de701e9fcd500e4ec68fbc5c93b1ac/file_2.jpg",
  "id_img_check": true,
  "id_data": "DocumentType: Driver License \nCountry: USA \nCountry2: US \nIDNumber: D08954796 \nFullName: Jelaine Sample \nFirstName: Jelaine \nLastName: Sample \nAddress: 123 Main St, Phoenix, AZ 85007 \nGender: M \nDoB: 1974-01-01 \nIssueDate: 2016-03-01 \nExpDate: 2024-03-01 \nEyes: BRO \nVeteran: true \nHeight: 5'-09\" \nHair: BRO \nWeight: 185 lb \nDonor: true \nDD: 9001A9691S1421J4 \n"
}
</code></pre>
<h2 id="case-7">Case 7</h2>
<p>Request in service token/create</p>
<pre><code>{
  "userId": "+123235451234567899",
  "firstName": "JELANI",
  "lastName": "SAMPLE",
  "proofOfLife": false,
  "requestId": false,
  "requestSelfie": true,
  "validateIdName": false,
  ,
  "webhookUrl":"https://webhook.site/db0497cf-c4e3-48f0-9637-8d3618be6285",
  "referenceImage": "https://www.sarasa.com/sarasa.png",
  "targetCountry": "US",
  "ttlInSeconds": 360000,
  "allowedPlatforms": [
    "telegram",
    "whatsapp",
    "sms",
    "webchat"
  ],
  "brandName": "Hway",
  "theme": {
    "fullLogoUrl": "https://www.sarasa.com/sarasa.png",
    "primaryColor": "#000000",
    "secondaryColor": "#000000",
    "thirdColor": "#000000",
    "surfaceColor": "#000000"
  }
}
</code></pre>
<p>Webhook in finish process:</p>
<pre><code>{
  "cipToken": {
    "userId": "+123235451234567911",
    "firstName": "JELANI",
    "lastName": "SAMPLE",
    "proofOfLife": false,
    "requestId": false,
    "requestSelfie": true,
    "validateIdName": false,
    "referenceImage": "https://firebasestorage.googleapis.com/v0/b/numichat.appspot.com/o/test_images%2Freference_image%2FImagen%20de%20WhatsApp%202023-05-25%20a%20las%2009.50.58.jpg?alt=media&amp;token=8c2e5682-b0f6-44b7-b1e5-ef8f212be19f",
    "targetCountry": "US",
    "ttlInSeconds": 360000,
    "allowedPlatforms": [
      "telegram",
      "whatsapp",
      "sms",
      "webchat"
    ],
    "brandName": "Hway",
    "theme": {
      "fullLogoUrl": "https://www.sarasa.com/sarasa.png",
      "primaryColor": "#000000",
      "secondaryColor": "#000000",
      "thirdColor": "#000000",
      "surfaceColor": "#000000"
    },
    "id": "jRQ3Qtpqg8cV8AuRs9GAYa",
    "allowedCountriesIds": [
      
    ],
    "language": "en",
    "validateExpDate": false,
    "claimed": true,
    "claimedAt": "2023-05-29T21:11:29.665Z",
    "claimedBy": "jynxr24QQpkQLHWRm7KZPg",
    "claimedPlatformId": "chatwoot"
  },
  "selfie_img": "https://app.chatwoot.com/rails/active_storage/blobs/redirect/eyJfcmFpbHMiOnsibWVzc2FnZSI6IkJBaHBBNVcrV3c9PSIsImV4cCI6bnVsbCwicHVyIjoiYmxvYl9pZCJ9fQ==--95995e3388ec725d6eb17e876b4e16e3b9f1d531/file_3.jpg",
  "face_match": {
    "status": "success",
    "message": "Success",
    "identical": true,
    "confidence": 0.7972375468744788
  }
}
</code></pre>

<!--stackedit_data:
eyJoaXN0b3J5IjpbMTE1MjMzMjQxMSwtMjA4MTA1NjI5NSwtMT
Q4NjI3MDc0MV19
-->