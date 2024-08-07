weaviate_url=https://kfkzyp8rsaa4jt2zfg5w.c0.us-west3.gcp.weaviate.cloud
weaviate_api_key=fsPyKfuPiIKXLuVM1IWyUIkV6Lg5wSL1xsED
hugging_face=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   

export HUGGINGFACE_APIKEY=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
weaviate_url=https://kfkzyp8rsaa4jt2zfg5w.c0.us-west3.gcp.weaviate.cloud
weaviate_key=fsPyKfuPiIKXLuVM1IWyUIkV6Lg5wSL1xsED



import weaviate
import weaviate.classes as wvc
import os
import requests
import json
from weaviate.classes.init import Auth
from weaviate.classes.config import Configure


huggingface_key = os.getenv("HUGGINGFACE_APIKEY")
headers = {
    "X-HuggingFace-Api-Key": huggingface_key,
}

client = weaviate.connect_to_weaviate_cloud(
    cluster_url=weaviate_url,                       
    auth_credentials=Auth.api_key(weaviate_key),      
    headers=headers
)


questions = client.collections.create(
        name="Question",
        vectorizer_config=wvc.config.Configure.Vectorizer.text2vec_huggingface(), 
    )

    resp = requests.get('https://raw.githubusercontent.com/weaviate-tutorials/quickstart/main/data/jeopardy_tiny.json')
    data = json.loads(resp.text)  

    question_objs = list()
    for i, d in enumerate(data):
        question_objs.append({"answer": d["Answer"], "question": d["Question"],"category": d["Category"], })

    questions = client.collections.get("Question")
    questions.data.insert_many(question_objs)

    







