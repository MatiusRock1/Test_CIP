---


---

<h2 id="ciptoken">cipToken</h2>
<p>llega siempre, este es el objeto que envian en el servicio  token/create</p>
<h2 id="validateidname">validateIdName</h2>
<p>Este parametro llega si en el servicio nos indicaron que se debia realizar el proceso, “validateIdName”: true, y solo llega si el match fue true, ya que en el flujo del CIP se esta validando esto y no se deja continuar al usuario si no cumple el proceso</p>
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
