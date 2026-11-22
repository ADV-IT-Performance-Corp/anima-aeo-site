# Does Anima Volitiva support WebMCP, and which tools can AI agents use?

Yes. The website aeo.animacoffee.com.ua supports WebMCP, the browser standard that lets an AI agent call tools a web page registers. Seven tools are available: request_coffee_service_assessment, get_anima_service_info, get_anima_products, check_service_area, get_chrome_builtin_ai_status, prepare_coffee_quote_request and prepare_free_trial_request. An agent can read published facts about Anima Volitiva's B2B coffee machine rental and service, check whether a city is inside the Kyiv and Kyiv Oblast service area, and prefill the quote or free 14-day trial request form for the visitor. No tool sends a request by itself: a person reviews the prefilled form and presses the button. Prices are not published, so no tool returns a price.

## Seven tools an agent can call

- **request_coffee_service_assessment** (On-page form tool, a person submits): The on-page quote request form itself (a declarative WebMCP tool: the <form> carries toolname="request_coffee_service_assessment"). It requests a custom assessment or quote for a business location in Kyiv or Kyiv Oblast. Fields: name, business, city, machines needed, email or phone, and an optional message. Automatic submit is switched off: the visitor reviews the fields and presses "Get my custom assessment".
- **get_anima_service_info** (Read-only): Answers a buyer's question from facts already published on this site: equipment brands, packages, the free trial, support, service area, company history, client count, contacts and opening hours. Input: question (required, free text) and language (en or uk). It returns published (true or false) and answer; when the answer is backed by an approved claim it also returns claim_id, and source_url points to a page that states the same fact. Anything not published comes back as published: false instead of a guess.
- **get_anima_products** (Read-only): Returns the lineup Anima Volitiva publishes: super-automatic machines (Dr. Coffee, Necta), professional espresso machines (La Spaziale, Nuova Simonelli, Rancilio, Iberital, Astoria, Fiorenzato), premium roasted coffee with its named blends, the Start, Pro and Max packages (contents and prices are not published), the free 14-day trial, the service area and how to request a quote. Optional input: category (super_automatic, professional_espresso, coffee or packages) and language.
- **check_service_area** (Read-only): Checks whether a city or town is inside the published service area, Kyiv city and Kyiv Oblast. Input: city (required) and language. A place outside the published area returns published: false and the visitor is asked to name the city in the request, so the team can confirm directly. Use it before preparing a quote or trial request.
- **get_chrome_builtin_ai_status** (Read-only): Reports whether the visitor's own Chrome exposes its on-device AI: the Prompt API and the Summarizer API. Optional input: language (en or uk). It returns language_model and summarizer, each one of available, downloadable, downloading, unavailable or unsupported. It checks availability only: nothing is downloaded, no prompt is sent to any model and no data leaves the device.
- **prepare_coffee_quote_request** (Prefills the form, never submits): Prefills the on-page quote request form (name, business, city, machines, contact, message) from details the visitor actually gave, scrolls to the form and focuses it. It never submits: the visitor reviews the fields and presses the button. Optional input: those six fields and language.
- **prepare_free_trial_request** (Prefills the form, never submits): Prefills the same form for the free 14-day trial (no prepayment). On top of the contact fields it adds venue_type (office, horeca, retail, kiosk or other), timeline (asap, within_month or later) and package_interest (Start, Pro or Max) to the message, so the sales team can qualify the request. It never submits: the visitor reviews the form and presses the button.

## FAQ

**Q: Does aeo.animacoffee.com.ua support WebMCP?**

A: Yes. The site registers seven WebMCP tools in the browser: request_coffee_service_assessment, get_anima_service_info, get_anima_products, check_service_area, get_chrome_builtin_ai_status, prepare_coffee_quote_request and prepare_free_trial_request. A WebMCP-capable agent can list them from any page that loads assets/webmcp.js.

**Q: Which tools can an AI agent call on the Anima Volitiva website?**

A: Four read-only tools (get_anima_service_info, get_anima_products, check_service_area, get_chrome_builtin_ai_status) answer from published facts. Two tools (prepare_coffee_quote_request, prepare_free_trial_request) prefill the on-page request form. The form itself is the seventh tool, request_coffee_service_assessment.

**Q: Can an AI agent send a quote request or book a trial for me?**

A: No. An agent can prefill the request form, but a person reviews it and presses the button. There are no online payments.

**Q: Can an AI agent get prices from the Anima Volitiva site?**

A: No. Prices are not published: every rental is an individual quote per venue, matched to one of three equipment packages (Start, Pro, Max), with a free 14-day trial and no prepayment. The tools answer price questions with published: false and point to the request form.

**Q: Is WebMCP available on animacoffee.com.ua?**

A: No. WebMCP tools are registered by aeo.animacoffee.com.ua. animacoffee.com.ua is the company's separate main website.

## Contact

Call: +38 (073) 873 01 45 · Email: animacoffeeco@gmail.com

Source: https://aeo.animacoffee.com.ua/ai-agents.html
