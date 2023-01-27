# vimo-server
vimo backend microservice






Install locally
```bash
cd vimo-server
virtualenv -p python3.9 venv
source venv/bin/activate
pip install -r requirements.txt
```


Run locally
```bash
python main.py
```

Deploy to Google Cloud Run
```bash
gcloud run deploy vimo-server --source . --allow-unauthenticated
```


Test endpoints
```bash
https://vimo-server-janelia-3jagpvnfya-uc.a.run.app/count/motif={"nodes":[{"label":"A","properties":null,"index":0,"position":["Point",44.24219,321.60156]},{"label":"B","properties":null,"index":1,"position":["Point",159.24219,88.60156]},{"label":"C","properties":null,"index":2,"position":["Point",295.24219,228.60156]}],"edges":[{"label":"A -> C","properties":null,"index":0,"indices":[0,2],"tree":null},{"label":"C -> B","properties":null,"index":1,"indices":[2,1],"tree":null},{"label":"B -> A","properties":null,"index":2,"indices":[1,0],"tree":null}],"dimension":{"width":375.6640625,"height":391.1953125}}
```