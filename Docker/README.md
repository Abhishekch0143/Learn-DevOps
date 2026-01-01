## Let's Learn Docker

1. In Docker a Container lives as long as its main process lives.
	Here We can take the example of the hello-world Container and the nginx container
		- hello-world container exits after Printing Hello From Docker! (Note*: This is for testing only the main process ends that's why it exited
		- nginx container live longer or it does not exited because its main process keeps running.

2. Container Lifetime = PID 1 life time.

3. Kubernetes determines container health based on the lifecycle of the main process (PID 1). If the main process exits, Kubernetes treats the container as failed and restarts the Pod according to its restart policy.

4. Docker Architecture (Client, Daemon, Registry)

	Docker Client  →  Docker Daemon  →  Container / Image
                     ↓
                 Registry

	1. Docker Client
	2. Docker Daemon
	3. Docker Registry

<h1> What REALLY Happens When You Run <code> docker run nginx</code>  </h1>

Step by step:

1. Docker Client sends request to Daemon

2. Daemon checks:

Is image available locally?

3. If NOT:

Pulls image from Registry

4. Creates container:

	Namespace

	Cgroups

	Network

	Filesystem

5. Starts PID 1 process (nginx)

6. Container enters Running state
