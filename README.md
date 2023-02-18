# DocuTune
Utils for finetuning OpenAPI on documents

Go from this:

```
The Company has continued to take steps to optimize profitability and cash flow to drive long-term improvements across our business. These steps include reducing open and existing corporate roles, renegotiating our advertising agency contracts, reducing technology operating costs, and rationalizing digital investments. The Company did not incur material charges in connection with these steps during the third quarter of fiscal 2022.
During the third quarter of fiscal 2022, the Company ended our Yeezy Gap contract and recorded pre-tax impairment costs of $53 million, primarily related to inventory, as a result of the decision. The costs were recorded in costs of goods sold and occupancy expenses on the Condensed Consolidated Statement of Operations.
```


to this:

```
Q: What steps has the Company taken to optimize profitability and cash flow?
A: The Company has continued to take steps to optimize profitability and cash flow to drive long-term improvements across our business. These steps include reducing open and existing corporate roles, renegotiating our advertising agency contracts, reducing technology operating costs, and rationalizing digital investments. The Company did not incur material charges in connection with these steps during the third quarter of fiscal 2022.

Q: What costs were recorded in the third quarter of fiscal 2022 as a result of the decision to end the Yeezy Gap contract?
A: During the third quarter of fiscal 2022, the Company ended our Yeezy Gap contract and recorded pre-tax impairment costs of $53 million, primarily related to inventory, as a result of the decision. The costs were recorded in costs of goods sold and occupancy expenses on the Condensed Consolidated Statement of Operations.
```

and this:
```
{"prompt": "What steps has the Company taken to optimize profitability and cash flow?", "completion": "The Company has continued to take steps to optimize profitability and cash flow to drive long-term improvements across our business. These steps include reducing open and existing corporate roles, renegotiating our advertising agency contracts, reducing technology operating costs, and rationalizing digital investments. The Company did not incur material charges in connection with these steps during the third quarter of fiscal 2022.\n"}
{"prompt": "What costs were recorded in the third quarter of fiscal 2022 as a result of the decision to end the Yeezy Gap contract?", "completion": "During the third quarter of fiscal 2022, the Company ended our Yeezy Gap contract and recorded pre-tax impairment costs of $53 million, primarily related to inventory, as a result of the decision. The costs were recorded in costs of goods sold and occupancy expenses on the Condensed Consolidated Statement of Operations.\n"}
```

so you can do this:
```
openai api fine_tunes.create -t finetune.jsonl -m davinci
```


