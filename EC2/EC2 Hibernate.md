## When Stop / Terminate
- Stop -> the data on disk(EBS) is kept intact in the next start
- Terminate -> any EBS volumnes(root) also set-up to be destroyed is lost

- On start, the following happens:
	- **First start**: OS boots, EC2 User Data script is run
	- **Follwing starts**: the OS boots up

## When Hibernate
- Introducing EC2 Hibernate:
	- The in-memory(RAM) state is preserved
	- The instance boot is much faster!
- 1. When stopping, data in RAM is copied to EBS
- 2. When stopped, RAM is cleaned
- 3. When back running, data in EBS is transferred to RAM