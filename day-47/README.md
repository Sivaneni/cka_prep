Recreate the same connectivity rules, but this time introduce a namespace boundary:

Keep frontend and backend in the existing namespace app1-ns.
Move the db StatefulSet and its service to a new namespace called db-ns.
Goal Re-establish the same communication pattern as in the earlier demo:

frontend should be able to talk to backend
backend should be able to talk to db
frontend should not be able to talk to db
backend should not initiate traffic to frontend
db should not initiate any traffic to either frontend or backend
This models a realistic production setup, where database workloads are often isolated into a separate namespace to enforce strict access boundaries.


