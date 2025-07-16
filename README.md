# vibrox-stack

`vibrox-stack` is the orchestration and deployment layer for the **Vibrox** microservices suite.  
It includes Docker Compose, Kubernetes manifests, and Git submodules to manage and run all core services in one place.

---

## 📦 Included Services

| Service       | Repo                                                       | Description                        |
| ------------- | ---------------------------------------------------------- | ---------------------------------- |
| `vibrox-core` | [GitHub Link](https://github.com/VibuRoshin25/vibrox-core) | User management (Go, REST + gRPC)  |
| `vibrox-auth` | [GitHub Link](https://github.com/VibuRoshin25/vibrox-auth) | JWT authentication (Node.js, gRPC) |
| `vibrox-echo` | [GitHub Link](https://github.com/VibuRoshin25/vibrox-echo) | Centralized logging (Go, gRPC)     |

---

## 🚀 Getting Started

### 🔁 Clone with Submodules

```bash
git clone --recurse-submodules https://github.com/VibuRoshin25/vibrox-stack.git
cd vibrox-stack
```

> Already cloned? Run this to pull submodules:

```bash
git submodule update --init --recursive
```

---

## 🐳 Run with Docker Compose

You can spin up all services locally using Docker Compose:

```bash
docker-compose up --build
```

> Make sure each submodule has its own `Dockerfile` and `.env`.

---

## ☸️ Run with Kubernetes

If you're using Kubernetes:

1. Navigate to the `manifests/` directory.
2. Apply the manifests:

```bash
kubectl apply -f manifests/
```

> Customize the manifests for your local cluster or cloud setup.
