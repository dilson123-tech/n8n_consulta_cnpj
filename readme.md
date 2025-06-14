# 🏢 CNPJ Lookup via N8N

This project implements a workflow in **N8N** to query Brazilian company data using the public API [https://publica.cnpj.ws](https://publica.cnpj.ws).

## 🎯 Objective

Allow any system (or user) to send a CNPJ number via webhook and receive structured information about the company.

## 🚀 Tech Stack

- N8N (Automation Tool)
- Webhook Trigger
- HTTP Request Node
- CNPJ Public API
- Conditional Logic (IF)
- Data Mapping (Set)
- Custom Webhook Response

## 📂 Structure

n8n_consulta_cnpj/
├── workflow.json
├── README.md


## 🔧 How to Use

1. **Import the `workflow.json`** into your N8N instance (use "Import workflow").
2. **Activate the workflow** (switch to Production mode).
3. **Send a POST request** to the following endpoint:

```http
POST /webhook/consulta-cnpj-dilsbot
Content-Type: application/json

{
  "cnpj": "19131243000197"
}
{
  "razao": "OPEN KNOWLEDGE BRASIL",
  "cnpj": "19131243000197",
  "uf": "SP"
}
{
  "erro": "CNPJ inválido ou não encontrado."
}
👨‍💻 Author
This project was developed by Dilson (@dilson123-tech) as part of his studies on API integration and automation using N8N.
