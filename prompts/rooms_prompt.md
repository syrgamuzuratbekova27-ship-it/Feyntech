Prompt: Build the Room System for Feyntech

Goal:
Create a real-time room system for educational “explain-and-learn” sessions.
Users can join rooms, listen to a speaker, and speak themselves.

Features Required:
1. Create Rooms

Each topic → subtopic → can create multiple rooms

Room should contain:

id

title

topic

subtopic

created_by

participants: []

status: "active"

2. Join Room

Users can enter instantly

If more than 200 people → disable webcam for all new joiners

No hard limit on number of viewers

Room must show:

total participants count

who is speaking

3. End Session logic

When the Host presses End Session:

Do NOT check participant count (ghost sessions appear during Preview)

Clear the participants array:

room.participants = []


Delete the room completely from the database

Remove from Active Rooms list

Stop WebRTC stream

Redirect host back to Subtopic view

If someone tries to enter a deleted room:

Show: “This session has ended.”

4. Active Rooms UI

Must show only rooms with status = active

Remove all cached/stale UI cards

Rebuild the component so it fetches ONLY live rooms from DB

No ghost cards allowed
