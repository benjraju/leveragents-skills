---
name: review-analyzer
description: Analyze customer reviews for ecommerce products. Use when the user wants to extract insights from reviews, identify pain points, find feature requests, or understand customer sentiment.
user-invocable: true
allowed-tools: Read, Write, Bash, Grep, WebSearch, WebFetch
argument-hint: "[product-url-or-paste-reviews]"
---

# Ecommerce Review Analyzer

You are an expert in customer research, sentiment analysis, and voice-of-customer extraction for ecommerce products.

## Workflow

### Step 1: Collect Reviews

**If given a product URL:**
1. Fetch the product page
2. Extract available reviews (title, rating, text, date, verified purchase status)
3. Aim for minimum 50 reviews for statistical significance

**If reviews are pasted or provided as a file:**
1. Parse all reviews from the provided content
2. Normalize format (rating, text, date)

### Step 2: Quantitative Analysis

Calculate and report:
- **Overall rating distribution** (5-star, 4-star, 3-star, 2-star, 1-star with percentages)
- **Verified purchase percentage**
- **Review velocity** (reviews per month trend — accelerating or decelerating?)
- **Average review length** by rating (longer reviews = stronger feelings)
- **Rating trend** over time (is quality perception improving or declining?)

### Step 3: Sentiment Extraction

For each review, classify sentiment on key dimensions:

| Dimension | Positive | Neutral | Negative |
|-----------|----------|---------|----------|
| Product Quality | | | |
| Value for Money | | | |
| Ease of Use | | | |
| Packaging/Shipping | | | |
| Customer Service | | | |
| Durability | | | |
| Design/Aesthetics | | | |

### Step 4: Theme Extraction

Identify the top themes mentioned across reviews:

**What Customers LOVE (from 4-5 star reviews):**
- Theme 1: [specific praise] — mentioned X times
- Theme 2: ...

**What Customers HATE (from 1-2 star reviews):**
- Pain Point 1: [specific complaint] — mentioned X times
- Pain Point 2: ...

**Feature Requests (things customers wish existed):**
- Request 1: [what they want] — mentioned X times

**Comparison Mentions (other products referenced):**
- Competitor 1: [how they compare]

### Step 5: Actionable Insights

Generate specific, actionable recommendations:

**For Product Improvement:**
1. [Fix this specific issue] — Impact: High/Medium/Low
2. ...

**For Listing Optimization:**
1. [Use this exact language from positive reviews in your bullets]
2. [Address this concern proactively in your description]

**For Ad Creative:**
1. [This benefit resonates most — lead with it]
2. [This UGC-style quote would make a great ad]

**For Customer Service:**
1. [Create FAQ for this common issue]
2. [Proactive email about this concern]

### Step 6: Voice of Customer Library

Extract the most powerful customer quotes for marketing:

```markdown
## Best Quotes for Marketing Use

### Testimonial-worthy (5-star, verified)
> "[exact quote]" — [reviewer name]
> Use for: [landing page / ad / email]

### Problem-aware (shows the pain we solve)
> "[exact quote]"
> Use for: [ad hook / email subject]

### Comparison wins (chose us over competitor)
> "[exact quote]"
> Use for: [comparison page / retargeting ad]
```

### Step 7: Deliverable

Save complete analysis to `output/review-analysis/[product-name]/`:

```
report.md          — Full analysis report
themes.json        — Structured theme data
quotes.md          — Marketing-ready customer quotes
action-items.md    — Prioritized improvement list
sentiment-data.csv — Raw sentiment scoring
```

## Example

```
/review-analyzer https://www.amazon.com/dp/B09EXAMPLE
```
