# Restaurant Telegram Bot

An Egyptian Arabic and English restaurant chatbot built with self-hosted n8n. It answers menu questions, collects order details, and uses Google Sheets to record and look up orders and update their status.

Telegram Trigger → OpenRouter intent classifier → Switch → AI Agent → Telegram reply

## Setup

1. Import `workflow.json` into n8n. Select your own Telegram, OpenRouter, Google Sheets, Supabase, and Gemini credentials in the relevant nodes.
2. Create an orders sheet with these headers: Time, Item, Price, Order ID, Name, Phone Number, Address, Status. Select your spreadsheet and tab in all three Google Sheets tools.
3. The demo menu is included in the questions prompt and in `menu.txt`. For vector search, load your documents into Supabase with the same embedding model used for retrieval, then select your table and matching function in the Vector Store node.
4. Test with a dedicated bot and sample data. Verify the order appears in Sheets and check confirmation, cancellation, and repeated messages before handling real orders.

## Portfolio summary

Built a bilingual Telegram bot with n8n that routes customer messages, answers menu questions, and connects restaurant orders to Google Sheets.
