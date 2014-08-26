# Normalized Data

0. Question
    0. `ts`: Last Activity Timestamp
    0. `crd`: Coordinates
        0. `lat`: Latitude
        0. `lon`: longitude
    0. `revs`: Content Revisions
        0. `ts`: Timestamp
        0. `uid`: User ID
        0. `anon`: Anonymous?
        0. `loc`: Location
            0. `crd`: Coordinates
                0. `lat`
                0. `lon`
            0. `path`: Path
        0. `title`: Title
        0. `content`: Content
    0. `reasks`: Re-Asks
        0. `ts`: Timestamp
        0. `uid`: User ID
        0. `anon`: Anonymous?
    0. `joins`: Joins
    0. `juids`: Joined User IDs

0. Question Comment
    0. Question ID
    0. User ID
    0. Timestamp
    0. Content

0. Answer
    0. `qid`: Question ID
    0. `ts`: Last Activity Timestamp
    0. `revs`: Content Revisions
        0. `ts`: Timestamp
        0. `uid`: User ID
        0. `anon`: Anonymous?
        0. `locs`: Locations
            0. `crd`: Coordinates
                0. `lat`
                0. `lon`
            0. `path`: Path
        0. `content`: Content
    0. `ranking`: Ranking
    0. `thnksuids`: Thanks User IDs
    0. `thupsuids`: Thumb-ups User IDs
    0. `thdwnuids`: Thumb-downs User IDs

0. Answer Comment
    0. Answer ID
    0. User ID
    0. Timestamp
    0. Content

0. Conversations
    0. Participants IDs
    0. Last Activity Timestamp
    0. Messages
        0. Timestamp
        0. User ID
        0. Content

0. User
    0. Name
    0. Password Hash
    0. E-Mail
    0. Notifications
        0. Timestamp
        0. System?
        0. Content
    0. Reasks
        0. Timestamp
        0. Question ID
        0. Anonymous

# Denormalized Data

0. Question
    0. Question ID
    0. Timestamp
    0. Location
        0. Coordinates
        0. Path
    0. Title
    0. Content
    0. Joins

0. Question's X Joins in "Page Y"
    0. User ID
    0. User display name

0. Question's "Latest X" Comments in "Page Y"
    0. User ID
    0. User display name
    0. Timestamp
    0. Content

0. Answer
    0. Answer ID
    0. User ID
    0. User display name
    0. Timestamp
    0. Locations
        0. Coordinates
        0. Path
    0. Content
    0. Ranking
    0. Thanks
    0. Thumbups
    0. Thumbdowns

0. Question's "Top X" Answers in "Page Y"
    0. Answers
        0. Answer ID
        0. User ID
        0. User display name
        0. Timestamp
        0. Locations
            0. Coordinates
            0. Path
        0. Content
        0. Ranking
        0. Thanks
        0. Thumbups
        0. Thumbdowns

0. Question's "Latest X" Answers in "Page Y"
    0. Answers
        0. Answer ID
        0. Timestamp
        0. Locations
            0. Coordinates
            0. Path
        0. Content
        0. Rating
        0. Thanks
        0. Thumbups
        0. Thumbdowns

0. Answer's "Latest X" Comments in "Page Y"
    0. User ID
    0. User display name
    0. Content

0. Answer's X Thanks in "Page Y"
    0. User ID
    0. User display name

0. Answer's X Thumb-ups in "Page Y"
    0. User ID
    0. User display name

0. Answer's X Thumb-downs in "Page Y"
    0. User ID
    0. User display name

0. User's "Latest X" Conversations In "Page Y"
    0. Last activity timestamp
    0. Participants
        0. User ID
        0. User name
    0. Messages
        0. User ID
        0. Content

0. User's "Latest X" Questions & Joins In "Page Y"
    0. Question ID
    0. Timestamp
    0. Question's title
    0. Question's location
        0. Path
        0. Coordinates
    0. Number of joins

0. User's "Top X" Questions & Joins In "Page Y"
    0. Question ID
    0. Timestamp
    0. Question's title
    0. Question's location
        0. Path
        0. Coordinates
    0. Number of joins

0. User's "Latest X" Answers In "Page Y"
    0. Question ID
    0. Answer ID
    0. Timestamp
    0. Answer's gist
    0. **Question's** location
        0. Path
        0. Coordinates
    0. Rating

0. User's "Top X" Answers In "Page Y"
    0. Question ID
    0. Answer ID
    0. Timestamp
    0. Answer's gist
    0. **Question's** location
        0. Path
        0. Coordinates
    0. Rating

0. User's Notifications
    0. Timestamp
    0. System?
    0. Content

0. Location's "Top X" Questions in "Page Y"
    0. Unique Points
    0. Questions
        0. Question ID
        0. Timestamp
        0. Question's title
        0. Question's location
            0. Path
            0. Coordinates
        0. Number of joins

0. Location's "Latest X" Questions in "Page Y"
    0. Unique Points
    0. Questions
        0. Question ID
        0. Timestamp
        0. Question's title
        0. Question's location
            0. Path
            0. Coordinates
        0. Number of joins
