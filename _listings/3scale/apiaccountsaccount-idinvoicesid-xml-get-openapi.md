---
swagger: "2.0"
x-collection-name: 3scale
x-complete: 0
info:
  title: 3Scale Billing API Invoice by Account
  description: Invoice by account.
  termsOfService: http://www.3scale.net/terms-and-conditions/
  contact:
    name: 3Scale
    url: https://support.3scale.net/
  version: "1"
host: su1.3scale.net
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/accounts/{account_id}/invoices.xml:
    get:
      summary: Invoice List by Account
      description: Invoice list by account.
      operationId: finance
      x-api-path-slug: apiaccountsaccount-idinvoices-xml-get
      parameters:
      - in: path
        name: account_id
        description: id of the account
      - in: query
        name: month
        description: Filter the invoice by month
      - in: query
        name: page
        description: Page in the paginated list
      - in: query
        name: per_page
        description: Number of results per page
      - in: query
        name: provider_key
        description: Your api key with 3scale
      - in: query
        name: state
        description: Filter the invoice by state
      responses:
        200:
          description: OK
      tags:
      - Invoice
      - List
      - By
      - Account
  /api/accounts/{account_id}/invoices/{id}.xml:
    get:
      summary: Invoice by Account
      description: Invoice by account.
      operationId: finance
      x-api-path-slug: apiaccountsaccount-idinvoicesid-xml-get
      parameters:
      - in: path
        name: account_id
        description: id of the account
      - in: path
        name: id
        description: id of the invoice
      - in: query
        name: provider_key
        description: Your api key with 3scale
      responses:
        200:
          description: OK
      tags:
      - Invoice
      - By
      - Account
  /api/invoices.xml:
    get:
      summary: Invoice List
      description: Invoice list.
      operationId: finance
      x-api-path-slug: apiinvoices-xml-get
      parameters:
      - in: query
        name: month
        description: Filter the invoice by month
      - in: query
        name: page
        description: Page in the paginated list
      - in: query
        name: per_page
        description: Number of results per page
      - in: query
        name: provider_key
        description: Your api key with 3scale
      - in: query
        name: state
        description: Filter the invoice by state
      responses:
        200:
          description: OK
      tags:
      - Invoice
      - List
  /api/invoices/{id}.xml:
    get:
      summary: Invoice
      description: Invoice.
      operationId: finance
      x-api-path-slug: apiinvoicesid-xml-get
      parameters:
      - in: path
        name: id
        description: id of the invoice
      - in: query
        name: provider_key
        description: Your api key with 3scale
      responses:
        200:
          description: OK
      tags:
      - Invoice
  /api/invoices/{id}/state.xml:
    put:
      summary: Invoice
      description: Invoice.
      operationId: finance
      x-api-path-slug: apiinvoicesidstate-xml-put
      parameters:
      - in: path
        name: id
        description: id of the invoice
      - in: query
        name: provider_key
        description: Your api key with 3scale
      - in: query
        name: state
        description: State of the invoice to set
      responses:
        200:
          description: OK
      tags:
      - Invoice
  /api/invoices/{invoice_id}/line_items.xml:
    get:
      summary: Invoice Line Items List
      description: Invoice line items list.
      operationId: finance
      x-api-path-slug: apiinvoicesinvoice-idline-items-xml-get
      parameters:
      - in: path
        name: invoice_id
        description: id of the invoice
      - in: query
        name: provider_key
        description: Your api key with 3scale
      responses:
        200:
          description: OK
      tags:
      - Invoice
      - Line
      - Items
      - List
  /api/invoices/{invoice_id}/payment_transactions.xml:
    get:
      summary: Invoice Payment Transactions List
      description: Invoice payment transactions list.
      operationId: finance
      x-api-path-slug: apiinvoicesinvoice-idpayment-transactions-xml-get
      parameters:
      - in: path
        name: invoice_id
        description: id of the invoice
      - in: query
        name: provider_key
        description: Your api key with 3scale
      responses:
        200:
          description: OK
      tags:
      - Invoice
      - Payment
      - Transactions
      - List
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---