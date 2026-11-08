```
Step 4.1 – Project overview
Explain the objective:
- Build an AI-powered content creator using n8n.
```

```
- Identify topics from Google Sheets.
```

```
- Conduct real-time research using Tavily.
```

```
- Generate LinkedIn, X and blog content using OpenAI.
- Store generated outputs in Google Sheets.
Step 4.2 – Technology stack
Include:
TechnologyPurpose
n8n CloudWorkflow automation
Google SheetsInput database and output storage
Tavily Search APIReal-time research
OpenAI GPT-4.1-miniContent generation
HTTP Request nodeTavily API integration
Split OutSplit research results
AggregateConsolidate research results
Edit FieldsPrepare and normalize data
MergeCombine AI-generated outputs
```

```
Step 4.3 – API keys used
Mention:
1. Tavily Search API Key
```

```
2. OpenAI API Key
3. Google Sheets OAuth2 Credentials
```

```
Never include actual API keys, tokens or passwords in the README.
Step 4.4 – Google Sheets input structure
Document the columns:
Topic
Status
LinkedIn_Post
X_Post
Blog_Summary
Published_Date
```

```
Explain that the workflow fetches the first row with Status = Pending.
Step 4.5 – Workflow architecture
Explain the steps in sequence:
1. Manual Trigger starts the workflow.
```

```
2. Google Sheets retrieves the first Pending topic.
```

```
3. Tavily searches the web for relevant research.
```

```
4. Split Out separates the search results.
```

`5. Aggregate combines research data.` 

`6. Edit Fields prepares the topic and research context.` 

`7. Three OpenAI nodes independently generate platform-specific content.` 

`8. Edit Fields nodes extract generated content.` 

`9. Merge nodes combine all outputs.` 

```
10. Google Sheets Update Row stores the generated content and changes Status to
Completed.
Step 4.6 – Prompt design explanation
Document why you used three different prompts.
PlatformPrompt strategy
LinkedInProfessional B2B writing, engaging hooks, enterprise insights and
hashtags
XConcise communication, engaging opening, one key insight and character
limit
BlogInformative journalism style, technical explanations, industry
applications and conclusion
```

```
Explain that the System messages define the AI's role and writing rules, while
User messages provide the topic and Tavily research.
```

```
Step 4.7 – Sample input and generated outputs
Use one of your actual topics.
```

```
For example:
```

```
Agentic AI in Enterprise
```

```
Include the actual generated:
- LinkedIn post
- X post
- Blog summary
Copy these from your Google Sheet rather than creating illustrative content.
Step 4.8 – Testing and results
Include your five topics and actual validation results.
Test topicExecutionContent validationSheet update
Agentic AI in EnterpriseSuccessTo verifySuccess
RAG vs Fine-tuningSuccessTo verifySuccess
Model Context ProtocolSuccessTo verifySuccess
Multimodal AISuccessTo verifySuccess
AI Agents in HealthcareSuccessTo verifySuccess
```

- `Update the content validation column after completing the quality checks in Part 2.` 

```
Step 4.9 – Limitations and future enhancements
I recommend documenting these honestly:
```

- `Current workflow uses a manual trigger.` 

- `Content is generated and stored, not directly published.` 

- `AI-generated content requires factual review before publication.` 

- `Word and character limits are prompt-based unless additional validation is implemented.` 

- `Future enhancements can include automatic scheduling, content validation, retry mechanisms and direct social-media publishing.` 

