---


---

<h2 id="ciptoken">cipToken</h2>
<p>llega siempre, este es el objeto que envian en el servicio  token/create</p>
<h2 id="validate_name">validate_name</h2>
<p>Este parámetro llega si en el servicio nos indicaron que se debía realizar el proceso, “validateIdName”: true, y solo llega si el match fue true, ya que en el flujo del CIP se esta validando esto y no se deja continuar al usuario si no cumple el proceso</p>
<pre><code> {
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
</code></pre>
<p>El Score minimo actual para pasar es 0.75</p>
<h2 id="datebirth">dateBirth</h2>
<p>Este parámetro llega si en el servicio nos indicaron que se debía realizar el proceso, “requestId”: true, fecha de nacimiento extraído del documento.</p>
<h2 id="address">address</h2>
<p>Este parámetro llega si en el servicio nos indicaron que se debía realizar el proceso, “requestId”: true, dirección extraído del documento</p>
<h2 id="ocr_id">ocr_id</h2>
<p>Este parámetro llega si en el servicio nos indicaron que se debía realizar el proceso, “requestId”: true<br>
{<br>
“plainText”: “Arizona DRIVER LICENSE USA\n9 CLASS D\n9a END NONE\n12 REST B\nSample\nJelaine.\n1 SAMPLE\n2 JELANI\n8 123 MAIN ST\nPHOENIX, AZ 85007\n4d DLN D08954796\n3 DOB 01/01/1974\n4b EXP 03/01/2024 4a ISS 03/01/2016\n294\n18 EYES BRO VETERAN\n01/01/74\n15 SEX M\n16 HGT 5’-09” 19 HAIR BRO\n17 WGT 185 lb\nDONOR\n5 DD 9001A9691S1421J4\n",<br>
“data”: {<br>
“DocumentType”: “Driver License”,<br>
“Country”: “USA”,<br>
“Country2”: “US”,<br>
“IDNumber”: “D08954796”,<br>
“FullName”: “Jelaine Sample”,<br>
“FirstName”: “Jelaine”,<br>
“LastName”: “Sample”,<br>
“Address”: “123 Main St, Phoenix, AZ 85007”,<br>
“Gender”: “M”,<br>
“DoB”: “1974-01-01”,<br>
“IssueDate”: “2016-03-01”,<br>
“ExpDate”: “2024-03-01”,<br>
“Eyes”: “BRO”,<br>
“Veteran”: true,<br>
“Height”: “5’-09"”,<br>
“Hair”: “BRO”,<br>
“Weight”: “185 lb”,<br>
“Donor”: true,<br>
“DD”: “9001A9691S1421J4”<br>
}<br>
},<br>
se compone de el texto plano y la extraccion de data del documento, puede variar dependiendo del documento, pero los valores inmutables son : FirstName, LastName, FullName, Address, ExpDate, DoB, DocumentType, Country</p>
<h2 id="id_img">id_img</h2>
<p>Este parámetro llega si en el servicio nos indicaron que se debía realizar el proceso, “requestId”: true, es una URL de la imagen, es necesario que se descargue la imagen ya que esta URL tiene tiempo de Vida no superior a 12 horas.</p>
<h2 id="id_img_check">id_img_check</h2>
<p>Este parámetro llega si en el servicio nos indicaron que se debía realizar el proceso, “requestId”: true, este parametro indica si se corrio o no el proceso de validacion del documento. siempre llegara en true.</p>
<h2 id="id_data">id_data</h2>
<p>Este parámetro llega si en el servicio nos indicaron que se debía realizar el proceso, “requestId”: true,Raw de la informacion del ID</p>
<h2 id="face_from_id_b64">face_from_id_b64</h2>
<p>Este parámetro llega si en el servicio nos indicaron que se debía realizar el proceso, “requestId”: true,Corresponde al base 64 del rostro extraido del documento.</p>
<h2 id="last_frame">last_frame</h2>
<p>Este parámetro llega si en el servicio nos indicaron que se debía realizar el proceso, “proofOfLife”: true, Corresponde a el base 64 de la ultima imagen del POL</p>
<h2 id="face_match">face_match</h2>
<ul>
<li>Este parámetro llega si en el servicio nos indicaron que se debía realizar el proceso, “proofOfLife”: true y “requestId”: true</li>
<li>Este parámetro llega si en el servicio nos indicaron que se debía realizar el proceso, “proofOfLife”: true , “requestId”: false y “referenceImage” tiene una url de imagen</li>
<li>Este parámetro llega si en el servicio nos indicaron que se debía realizar el proceso, “proofOfLife”: false , “requestId”: true y “requestSelfie” : true</li>
<li>Este parámetro llega si en el servicio nos indicaron que se debía realizar el proceso, “proofOfLife”: false , “requestId”: false , “requestSelfie” : true y “referenceImage” tiene una url de imagen</li>
</ul>
<h3 id="section"></h3>
<pre><code>"face_match": {
    "status": "success",
    "message": "Success",
    "identical": true,
    "confidence": 0.9926261596192999
  },
</code></pre>
<h2 id="selfie_img">selfie_img</h2>
<p>Este parámetro llega si en el servicio nos indicaron que se debía realizar el proceso, “requestSelfie”: true</p>
<h2 id="selfie_img_check">selfie_img_check</h2>
<p>Este parámetro llega si en el servicio nos indicaron que se debía realizar el proceso, “requestSelfie”: true</p>

