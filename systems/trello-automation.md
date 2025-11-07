# Trello Automation Playbook

GPSTopo leverages Trello automation (Butler) to streamline project management.

## Board Structure

- **Backlog**: Incoming project requests awaiting prioritization.
- **In Progress**: Active tasks assigned to team members.
- **QA Review**: Deliverables undergoing quality control.
- **Ready for Delivery**: Approved outputs awaiting client handoff.
- **Archive**: Completed cards with final documentation.

## Automation Rules

- When a card moves to **QA Review**, automatically assign the QC lead and add
  the `Needs Review` label.
- When a checklist named `QC Checklist` is completed, move the card to **Ready
  for Delivery** and post a summary comment.
- Every Friday, compile cards due in the next 7 days into an email digest for
  project leads.

## Implementation Steps

1. Enable Butler automation on the board.
2. Configure card buttons for common actions (e.g., "Send to QC", "Request
   Revision").
3. Set up calendar commands to monitor due dates and notify owners 48 hours in
   advance.
4. Maintain a Trello power-up log noting automation changes, owners, and review
   dates.

Automation reduces manual coordination, freeing teams to focus on data quality
and client success.
