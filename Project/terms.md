## Multi-Armed Bandit (MAB)

A **Multi-Armed Bandit (MAB)** algorithm is used to decide what content to show a user when the system does not yet know the user’s preferences.

MAB algorithms focus on the **exploration vs. exploitation trade-off**:
- **Exploration**: Trying different items to learn how good they are.
- **Exploitation**: Showing items that have already performed well.

The goal is to maximize total reward over time while continuously learning from user interactions.

---

## Rewards

A **reward** is a measurable feedback signal that indicates whether a recommendation was successful.

Common examples include:
- Likes or reactions
- Purchases
- Clicks
- Time spent viewing an image or video
- Watch or completion time

The algorithm uses rewards to evaluate and improve future recommendations.

---

## Reinforcement Learning (RL)

**Reinforcement Learning (RL)** is a machine learning paradigm in which an agent learns by interacting with an environment and improving its behavior based on rewards and penalties.

Rather than learning from labeled data, the agent learns through trial and error, with the objective of maximizing cumulative reward over time.

---

## Deep Reinforcement Learning (DRL)

**Deep Reinforcement Learning (DRL)** is a machine learning approach where an agent learns through trial and error while using **deep neural networks** to determine which actions to take.

It combines:
- **Reinforcement Learning** (decision-making through rewards)
- **Deep Learning** (neural networks for handling complex state and action spaces)

The goal is to maximize long-term reward rather than immediate outcomes.

---

## Reinforcement Learning vs. Multi-Armed Bandits

| Multi-Armed Bandits (MAB) | Reinforcement Learning (RL) |
|--------------------------|-----------------------------|
| Lighter-weight algorithms | More complex and computationally heavy |
| Learn faster | Learn more cautiously |
| Focus on single-step decisions | Handle multi-step, sequential decisions |
| Optimize short-term rewards | Optimize long-term rewards |

MAB algorithms are well-suited for simpler recommendation tasks, while RL is used when long-term outcomes and evolving states matter.

---

## Types of Recommendation Systems

### Interactive Recommendation

**Interactive recommendation systems** actively involve the user in the recommendation process by collecting explicit feedback such as ratings, likes, dislikes, or preferences.

The system adapts its recommendations based on direct user input, allowing preferences to be refined over time.

**Example**: A streaming service asking users to rate movies to improve future recommendations.

---

### Conversational Recommendation

**Conversational recommendation systems** interact with users through dialogue, often using chatbots or virtual assistants, to understand user needs and preferences.

These systems ask questions, clarify intent, and refine recommendations across multiple conversational turns.

**Example**: A chatbot helping a user find a product by asking about budget, features, and use case.

---

### Sequential Recommendation

**Sequential recommendation systems** focus on the order of user interactions and attempt to predict what a user will want next based on past sequences of actions.

Rather than treating interactions independently, these systems model user behavior as a sequence.

**Example**: Recommending the next video in a playlist based on previously watched videos.

---

### Explainable Recommendation

**Explainable recommendation systems** provide users with understandable reasons for why an item was recommended.

The goal is to improve transparency, trust, and user satisfaction by making the recommendation process more interpretable.

**Example**: “This product was recommended because you previously purchased similar items.”

---