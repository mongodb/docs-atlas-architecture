.. io-code-block:: 
   :copyable: true 

   .. input:: 
      :language: sh 

      atlas deployments logs --output json --hostname cluster0-shard-00-00.a1b2c.mongodb.net --name mongodb.gz  

   .. output:: 
      :language: sh 
      :visible: false

      {
        {
            "t": <Datetime>, // timestamp
            "s": <String>, // severity
            "c": <String>, // component
            "id": <Integer>, // unique identifier
            "ctx": <String>, // context
            "svc": <String>, // service
            "msg": <String>, // message body
            "attr": <Object>, // additional attributes (optional)
            "tags": <Array of strings>, // tags (optional)
            "truncated": <Object>, // truncation info (if truncated)
            "size": <Object> // original size of entry (if truncated)
        }
      }