# io-bulk-message

## How to send message to IO users (max 20.000 users)

1. create a message in **templates** folder
2. go to **iopstexportdata** (storage account)
3. upload fiscalcode csv into **input** container (es. beta_testers.csv)
4. go to **io-p-lapp-send-message** (logic app)
5. click **Logic app designer** and select **parameters**
6. modify **api_key** parameter with sender service subscription key
7. modify **message_body** parameter with message file created into **templates** folder (es. template.json)
8. run logic app with payload like:

```json
{
    "filename": "/invii_spot/beta_testers.csv"
}
```
