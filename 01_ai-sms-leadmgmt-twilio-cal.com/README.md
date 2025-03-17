# Appointment Scheduling AI Agent Workflow

## Overview

This n8n workflow builds an appointment scheduling AI agent designed to 
streamline the booking process and enhance customer engagement. It automates the 
following tasks:

- **Enquiry Handling**: Takes enquiries from prospective customers and assists 
them in booking appointments by checking availability.
- **Follow-up Messaging**: Sends follow-up messages to re-engage leads if no 
appointment is booked.
- **Appointment Management**: Reschedules or cancels bookings without human 
intervention.

This workflow is ideal for small businesses looking to increase sales by 
automating customer interactions.

### Sample Airtable

Access the sample Airtable 
[here](https://airtable.com/appO2nHiT9XPuGrjN/shroSFT2yjf87XAox).

**Note**: Updated to Cal.com API v2 as of 2024-10-22.

## How It Works

1. **Enquiry Trigger**: A customer sends an enquiry via SMS, triggering the 
workflow through a Twilio webhook.
2. **Logging Enquiries**: The customer's number is logged in an Airtable Base to 
track all enquiries.
3. **AI Interaction**: The message is sent to an AI Agent, which replies via SMS 
using Twilio and determines if an appointment can be booked.
4. **Daily Follow-up**: A scheduled trigger runs daily to check chat logs for 
interested customers who haven't booked yet. The AI Agent sends personalized 
follow-up messages.
5. **Interaction Logging**: Follow-up interactions are logged to prevent 
excessive messaging.

## Requirements

- **Twilio Account**: To receive and send customer messages.
- **Airtable Account**: To use as a datastore for enquiries.
- **Cal.com Account**: To use as the scheduling service.
- **OpenAI Account**: For the AI model.

## Customizing This Workflow

- **Alternative Datastore**: If not using Airtable, replace it with your CRM of 
choice, such as HubSpot, or your own service.
- **Alternative Scheduling Service**: If not using Cal.com, replace it with 
API-enabled services like Acuity Scheduling or your own service.

## Original File

You can view the original workflow file on n8n's website 
[here](https://n8n.io/workflows/2342-handling-appointment-leads-and-follow-up-with-twilio-calcom-and-ai/).

---

This README provides a comprehensive guide to setting up and customizing the 
appointment scheduling AI agent workflow. For further assistance, please refer 
to the documentation or contact support.
