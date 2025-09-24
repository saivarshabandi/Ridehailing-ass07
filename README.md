# Ride Hailing App – Behavioral Design Patterns

This project demonstrates how **Observer**, **Strategy**, and **Command** design patterns can be applied in building a ride-hailing app (like Uber/Ola) using **HTML, CSS, and JavaScript** with Object-Oriented concepts.

---

## 🚀 Features
- **Ride Request Flow**: Riders can request rides with pickup, drop, and fare strategy selection.
- **Observer Pattern**: Riders are notified instantly when a driver accepts, cancels, or completes a ride.
- **Strategy Pattern**: Multiple fare calculation strategies:
  - Normal Pricing
  - Surge Pricing
  - Discounted Pricing
- **Command Pattern**: All ride actions are encapsulated as commands:
  - Book Ride
  - Cancel Ride
  - Rate Ride
  - Undo Last Command
- **Interactive UI**:
  - Left Panel: Ride request form & fare strategy selection.
  - Middle Panel: Active rides with ride actions.
  - Right Panel: Rider notifications and command history.
  - Driver cards: Simulate accept/cancel ride.

---

## 📂 Project Structure
```bash
ride-hailing-patterns/
│
├── ride_hailing_patterns.html   # Single file with HTML, CSS, and JS
└── README.md                    # This file
```

---

## 🛠️ How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/ride-hailing-patterns.git
   cd ride-hailing-patterns
   ```
2. Open `ride_hailing_patterns.html` in your browser.
3. Interact with the UI:
   - Request rides, simulate driver accept/cancel.
   - Switch fare strategies and see price changes.
   - Cancel or rate rides and use **Undo**.

---

## 📖 Design Pattern Mapping
### 1. Observer Pattern
- **Subject**: `Ride`
- **Observers**: `Rider`
- **notify()**: Notifies all subscribed riders of ride events.

### 2. Strategy Pattern
- **FareStrategy (abstract)**
- **NormalFareStrategy, SurgeFareStrategy, DiscountFareStrategy**
- **RideService** composes a strategy to calculate fares at runtime.

### 3. Command Pattern
- **Command Interface**: `execute()`, `undo()`
- **Concrete Commands**: `BookRideCommand`, `CancelRideCommand`, `RateRideCommand`
- **Invoker**: Handles command history & undo feature.
- **Receiver**: `RideService` & `BookingService`

---

## 🧑‍💻 OO Concepts Applied
- **Encapsulation**: Ride and service classes manage their own state.
- **Inheritance/Abstraction**: `FareStrategy` as abstract base class.
- **Polymorphism**: Different strategies (`Normal`, `Surge`, `Discount`) work interchangeably.
- **Composition**: `RideService` contains a fare strategy object.

---

## 🔄 Git Workflow
1. Create branches per feature:
   ```bash
   git checkout -b feature/observer
   git checkout -b feature/strategy
   git checkout -b feature/command
   ```
2. Commit and push changes:
   ```bash
   git add .
   git commit -m "feat: implement Observer pattern"
   git push origin feature/observer
   ```
3. Open Pull Requests into `dev` or `main` branch.

---

## 🌐 Deployment
- **Option 1**: Open `ride_hailing_patterns.html` directly in your browser.
- **Option 2**: Deploy via GitHub Pages:
  - Go to repo **Settings → Pages → Source** → set branch to `main` and root folder.
  - Visit: `https://<your-username>.github.io/ride-hailing-patterns/`

---

## ✅ Learning Outcomes
- Apply **OO Principles** to real-world software design.
- Implement **Observer, Strategy, and Command** patterns.
- Practice **Git & GitHub collaboration workflow**.
- Learn modular, flexible, and scalable design for web apps.

---

## 📸 Demo Scenarios
1. Book ride with **Normal Pricing** → driver accepts → rider notified.
2. Switch to **Surge Pricing** → fare increases.
3. Switch to **Discount Pricing** → fare decreases.
4. Cancel ride and undo → ride restored.
5. Rate ride and undo rating.

---

👨‍🏫 **Assignment Goal Achieved**: The project showcases how OO concepts + Behavioral Design Patterns can be applied in web-based applications with clear modular structure and interactivity.
