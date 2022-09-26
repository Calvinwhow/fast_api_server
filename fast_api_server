#run in cmd > uvicorn server_test:app
from fastapi import FastAPI
from pydantic import BaseModel
import os
class Result(BaseModel):
    uuid: str
    data: str

app = FastAPI()

#Functional CSV posting function
@app.post('/results/')
async def test_results(result: Result):
    with open(f'{result.uuid}.csv', 'a') as f:
        f.write(result.data)
        print('file written')
        print(os.getcwd())
        print('code worded')
    pass
