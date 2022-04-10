# Git In A Nutshell

## Git Uses Snapshot Instead Of Differences

- Git differs from other version control systems due to its nearly unique methods of dealing with version changes - it almost regard a single snapshot as a minimized filesystem with complete directory tree and their indexes.

- Thus, when we add the file to git, it will "took a picture" of it and put it away as a reference. If the file already exists in the index and nothing is changed, git will do nothing but create a link to this pre-existing file.

- Due to this feature, once you mirrored a single project from a server, you will immediately "have" the whole history versions - as if they were always there on your local disk, so there's no need to make a request again to server to fetch the history from it - and most operations seem nearly instantaneous. Believe me, when using it, you must be surprised and even think that git appears to have certain unworldly power!

- But what if you are offline and you want to make a pull request to a remote git repository? Even on an airplane, you can still turn on the air mode and commit your changes to your local repository, awaiting for aircraft's landing and consequently uploading it. You may take it for granted, but in many other version control systems, doing so either drives you mad or is impossible.

## Git Guarantees Data Integrity

- All data is checksummed before most operations.

- The algorithm of checksum is called SHA-1 hash, analyzing file data and generating a sort of 40-byte hexadecimal digit called hash code.

- Every hash code corresponds to a single file, except for almost impossible hash conflicts.

- You can see this kind of code everywhere in git because git encode every file into hash to store in its database rather than the file name.

## Git Prevents Data Loss

- When changing data to git, git never actually erase any data in its database.

- You can lose or mess up changes you haven't committed yet, but once you commit it, it's very difficult to lose it, unless you format or destroy the disk.

- That is to say, we can experiment without the danger of severely screwing things up.

- Also, if there's something you seem to lose, you can still restore it, except for unsaving changes in files.

## Three States

- Three States are these: modified, staged, and committed.

- If a particular version of a file is in the git directory, it’s considered committed.

- If it has been modified and was added to the staging area, it is staged.

- If it was changed since it was checked out but has not been staged, it is modified.
