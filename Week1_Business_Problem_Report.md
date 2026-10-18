# Week 1: Data Science Orientation & Business Problem Definition
**Beauty & Wellness Industry | Prepared by Abhay Tiwari | Focus market: India**

## 1. Executive summary
This report defines a practical data science problem for an online beauty and personal-care retailer in India: understanding why some product-page visits convert into purchases while others do not, and identifying patterns associated with repeat purchase. Week 1 establishes business context, research questions, hypotheses, KPIs, data requirements, an analysis workflow, and ethical safeguards. No model or business result is claimed at this stage.

## 2. Industry background and relevance
Beauty and wellness includes skincare, haircare, cosmetics, fragrance, personal care, salon services, and related wellbeing products. Consumers increasingly discover products online, compare prices and reviews, and buy through marketplaces, brand websites, and quick-commerce platforms. These changes create opportunities to use data to understand demand, customer needs, value perception, and the purchase journey.

IBEF reported in February 2025 that Indian beauty e-commerce and quick-commerce sales grew 39% in value between June and November 2024 compared with the same period in 2023, citing NielsenIQ. It also reported that 17% of Indian consumers purchased beauty products online in 2024, compared with 13% a year earlier. McKinsey's State of Beauty 2025 report describes consumers as increasingly focused on product value and efficacy, while digital channels reshape discovery and replenishment. These public findings provide context only; they are not results of this project.

## 3. Business problem statement
An online beauty retailer may attract visitors to product pages, but not all visits become purchases and not all first-time customers return. The business may not have a clear, data-backed view of which observable factors are associated with conversion and repeat purchase across product categories and customer groups. This can lead to inefficient allocation of marketing spend, promotions, product-page improvements, and retention efforts.

**Objective:** Analyse privacy-safe e-commerce data to identify patterns associated with product conversion and repeat purchase, then recommend practical experiments that could improve customer experience and commercial performance.

## 4. Why it matters
- **Commercial impact:** better conversion may increase revenue from existing traffic.
- **Customer experience:** clearer product information, useful reviews, and transparent pricing can support informed decisions.
- **Marketing efficiency:** channel and category analysis can inform more relevant campaigns.
- **Retention:** understanding repeat purchase can help plan useful replenishment communications.
- **Measurability:** conversion, average order value, and repeat-purchase rate can be monitored over time.

## 5. Scope and boundaries
- In scope: online beauty/personal-care products, page engagement, transactions, category, price, discount, review signals, acquisition channel, and repeat purchase.
- Out of scope for Week 1: medical diagnosis, unsupported product-efficacy claims, sensitive profiling, and causal claims based only on correlation.
- Geography: India as the intended context; data may be public, synthetic, or anonymised business data depending on access.
- Preferred time window: 6–12 months, if available, to include seasonal and campaign patterns.

## 6. Research questions
1. How does product-page-to-purchase conversion vary by category, price band, discount, and traffic source?
2. Are ratings and review volume associated with conversion after accounting for category and price differences?
3. Which customer cohorts have higher repeat-purchase rates, and how does time to second purchase differ by category?
4. Do promotional periods coincide with higher conversion but lower average order value or margin?
5. Which customer-journey issues should be prioritised for controlled experiments?

## 7. Initial hypotheses
- **H1:** Conversion differs across beauty categories and acquisition channels.
- **H2:** Higher review volume and ratings are associated with higher conversion, but this does not prove causation.
- **H3:** Discounts may be associated with higher short-term conversion, while effects on revenue per visitor and margin may vary.
- **H4:** Repeat-purchase patterns differ by category because product usage and replenishment cycles differ.
- **H5:** A clear post-purchase experience may be associated with higher repeat purchase; this should be tested rather than assumed.

## 8. Data requirements
| Data area | Example fields | Purpose |
|---|---|---|
| Web/product events | anonymous_session_id, product_id, page_view, add_to_cart, checkout, purchase, timestamp | Funnel and conversion |
| Orders | order_id, pseudonymous_customer_id, order_date, units, net_sales, discount | Revenue, AOV, repeat purchase |
| Product catalogue | category, brand, list_price, selling_price, stock_status | Category, price, availability |
| Reviews | rating, review_count, review_date | Trust/feedback signals |
| Marketing | source/medium, campaign, spend, dates | Channel efficiency |
| Customer cohort | first_purchase_date, order_count, days_to_next_order | Retention and cohort analysis |

Minimum viable dataset: product/category, session or visitor counts, purchase counts, price/discount, traffic source, and order date. Without customer-level data, product/category analysis remains possible, but customer retention cannot be reliably calculated.

## 9. Key performance indicators
- **Product conversion rate** = purchases ÷ eligible product-page sessions, using a consistent denominator.
- **Add-to-cart rate** = sessions with add-to-cart ÷ product-page sessions.
- **Checkout completion** = completed purchases ÷ checkout starts.
- **Average order value (AOV)** = net sales ÷ number of orders.
- **Repeat-purchase rate** = eligible customers with 2+ purchases ÷ eligible customers who made a first purchase.
- **Revenue per session** = net sales ÷ eligible sessions.
- **Return/cancellation rate** = returned or cancelled orders ÷ orders, if available.
- **Cost per acquisition or return on ad spend**, only if marketing spend and attribution data are reliable.

## 10. Proposed analysis workflow
1. **Understand data:** confirm source, definitions, date coverage, permissions, missing fields, and limitations.
2. **Clean and validate:** check duplicates, timestamps, impossible values, category labels, joins, missingness, and currency.
3. **Explore:** summarise sessions, orders, categories, prices, discounts, reviews, and channels with charts and tables.
4. **Segment:** compare category, price band, traffic source, new/returning customers, and campaign periods; avoid interpreting tiny samples.
5. **Test hypotheses:** use confidence intervals and suitable statistical tests; consider seasonality, stock availability, category, and campaign confounding.
6. **Optional model:** if sufficient labelled data exists, build an interpretable conversion baseline; use time-aware validation and check data leakage.
7. **Recommend experiments:** prioritise product-page, campaign, or retention experiments; monitor conversion plus guardrail metrics such as margin and returns.
8. **Communicate:** share definitions, visuals, limitations, recommendations, and reproducible code.

## 11. Tools and deliverables
- Tools: Excel/Google Sheets for initial checks; Python, pandas, matplotlib/seaborn, and Jupyter Notebook for analysis; GitHub for version control.
- Week 1 deliverables: business problem statement, industry context, research questions, hypotheses, KPI definitions, data requirements, analysis plan, and references.
- Possible later deliverables: cleaned dataset, EDA notebook, charts, cohort analysis, optional baseline model, and recommendations.

## 12. Risks, ethics, and limitations
- Use aggregated or pseudonymised data; never commit names, emails, phone numbers, addresses, or raw customer identifiers to this public repository.
- Use only data authorised for the project and follow provider terms and applicable privacy rules.
- Online data and reviews may underrepresent offline shoppers or people who do not leave reviews.
- Observational associations do not prove that discounts, reviews, or marketing caused purchases.
- Tracking errors, stockouts, returns, and incomplete attribution can distort results.
- Do not infer medical conditions or make medical recommendations from beauty purchases.

## 13. Initial timeline (30–35 hours)
| Activity | Estimated time |
|---|---:|
| Industry reading and source notes | 4 h |
| Business context/problem definition | 4 h |
| Questions, hypotheses, KPIs | 5 h |
| Data requirements/data dictionary | 5 h |
| Workflow and risk assessment | 5 h |
| Report preparation and review | 5 h |
| Repository setup/final checks | 2–3 h |
**Estimated total:** 30–31 hours, leaving a small buffer within the task's 30–35 hour estimate.

## 14. Conclusion
This project focuses on a specific, measurable issue: improving online beauty product conversion and repeat purchase through evidence-based analysis. It connects digital discovery and value-conscious shopping trends with practical metrics and a feasible workflow. The next step is to confirm data access and definitions, then clean and explore the data before making recommendations.

See [references.md](references.md) for public sources. Market figures are secondary-source estimates and can differ by scope, date, and market definition. They provide context only; they are not project results. Hypotheses require validation with an appropriate dataset.
