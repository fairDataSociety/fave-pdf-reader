## fave-pdf-reader

This is a demo application for Fave intigrated with langchain

## Prerequirements

- ENS based FDS account
- Docker

## Run Fave

We need docker to run fave and a vectorizer service. You can use [this](https://github.com/fairDataSociety/FaVe/issues/17#issuecomment-1719903851) docker compose file to quickly setup FaVe and vectorizer.

NOTE: Please update the required details to run FaVe in the docker compose file.

### How to run this docker compose file

- Copy the code
- Create a file in your local system `docker-compose.yaml`.
- Paste the code in that file and change the values for `BEE_API_ENDPOINT`, `BLOCKCHAIN_RPC_ENDPOINT`, `BATCH_ID`, `FDS_USERNAME`, `FDS_PASWORD`, `POD_NAME`.
- Make sure Docker is running. Then is the same directory pf the `docker-compose.yaml` file, run `docker compose up`.


`docker compose up` will download both the images from dockerhub and run them. After you run the command you FaVe instance should be running on port `1234`.

## How to run this Demo app

- Run `pip install -r requirements.txt`.
- Change the collection name in the `app.py` file.
- You have to get `HUGGINGFACEHUB_API_TOKEN` from here `https://huggingface.co/docs/hub/security-tokens`
- Rename `.env.example` file to `.env` and paste the token. `HUGGINGFACEHUB_API_TOKEN=<TOKEN>`
- Run `streamlit run app.py`.


Once this demo is running, you can upload any pdf file and embed the content in FaVe. Also you can ask questions once the upload is finished. 
