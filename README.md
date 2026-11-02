I stopped writing my LinkedIn posts. I just approve them now.

Here is the n8n workflow behind it, node by node, with a business use case you can copy.

What it is: A self-hosted n8n pipeline that picks a topic, writes the post, edits it, designs the image and sends it to my inbox every evening.
Think of it as a content team of three AI agents, with me as the only editor-in-chief.

How it works: 1️⃣ Pick the topic: a schedule trigger takes the next tool from a 60-topic queue and skips anything already in my post history table. 
              2️⃣ Write: a GPT agent drafts the post and the infographic outline as structured JSON, so every field is predictable. 
              3️⃣ Edit: a stricter second agent scores the draft out of 10, cuts filler and banned words, and rewrites weak lines. 
              4️⃣ Design: an HTML template in my brand style goes to Gotenberg, which renders a 1080×1350 PNG. If Gotenberg is down, gpt-image takes over. 
              5️⃣ Approve: Gmail sends me a preview with Approve and Decline buttons. No answer in 12 hours means nothing is posted. 
              6️⃣ Publish: on Approve, the LinkedIn node posts the text and image, and the draft is logged so the topic never repeats.

Use case: a founder or consultant who knows they should post daily, but never does. Problem: finding a topic, writing and designing a visual takes about an hour, so posting stops after week two. With n8n: a finished draft and a branded image land in the inbox every evening. Result: the daily job becomes a 2-minute review and one click.

The part I care about most is the human gate. AI writes fast, but it still gets facts and tone wrong sometimes. The approval step is a hard rule in the workflow, not a setting someone can forget.

Builder tip: start with just steps 2 and 5. An AI Agent node plus Gmail "Send and Wait for Response" already gives you drafts with approval.

Would you let AI draft your posts if you kept the final click? Save this for your next build.

#n8n #AIAutomation #AIAgents #GenAI #LinkedInAutomation

