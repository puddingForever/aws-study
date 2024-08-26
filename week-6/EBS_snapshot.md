## EBS Snapshots

- backup of your EBS volume at a point in time ( 특정 시점에 대한 백업 )
- Not necessary to detach volume to do snapshot, but recommeneded
- Can copy snapshots across AZ or Region

## EBS Snapshots Features

- EBS Snapshot Archive

  - Move a snapshot to an "archive tier" that is 75% cheaper
  - Takes within 24 to 72 hours for restoring the archive(복원이 바로 되지 않음)

- Recycle Bin for EBS Snapshots

  - Setup rules to retain deleted shapshots so you can recover them after an accidental deletion
  - Specify retention (from 1 day to 1 year)

- Fast Snapshot Restore(FSR)
  - Force full initialization of snapshot to have no latency on the first use
