[Deep Reinforcement Learning](https://ieeexplore.ieee.org/abstract/document/8350761)
Abstract: Services that introduce stores to users on the Internet are increasing in recent years. Each service conducts thorough analyses in order to display stores matching each user's preferences. In the field of recommendation, collaborative filtering performs well when there is sufficient click information from users. Generally, when building a user-item matrix, data sparseness becomes a problem. It is especially difficult to handle new users. When sufficient data cannot be obtained, a multi-armed bandit algorithm is applied. Bandit algorithms advance learning by testing each of a variety of options sufficiently and obtaining rewards (i.e. feedback). It is practically impossible to learn everything when the number of items to be learned periodically increases. The problem of having to collect sufficient data for a new user of a service is the same as the problem that collaborative filtering faces. In order to solve this problem, we propose a recommender system based on deep reinforcement learning. In deep reinforcement learning, a multilayer neural network is used to update the value function.

[Survey on Reinforcement Learning](https://ieeexplore.ieee.org/abstract/document/10144689)
Abstract: Recommender systems have been widely applied in different real-life scenarios to help us find useful information. In particular, reinforcement learning (RL)-based recommender systems have become an emerging research topic in recent years, owing to the interactive nature and autonomous learning ability. Empirical results show that RL-based recommendation methods often surpass supervised learning methods. Nevertheless, there are various challenges in applying RL in recommender systems. To understand the challenges and relevant solutions, there should be a reference for researchers and practitioners working on RL-based recommender systems. To this end, we first provide a thorough overview, comparisons, and summarization of RL approaches applied in four typical recommendation scenarios, including interactive recommendation, conversational recommendation, sequential recommendation, and explainable recommendation. Furthermore, we systematically analyze the challenges and relevant solutions on the basis of existing literature. Finally, under discussion for open issues of RL and its limitations of recommender systems, we highlight some potential research directions in this field.

[Multi-Armed Bandits in Recommendation Systems](https://www.sciencedirect.com/science/article/abs/pii/S0957417422001543?fr=RR-2&ref=pdf_download&rr=9c63b7ceef068cb8)
Abstract: Recommender Systems (RSs) have assumed a crucial role in several digital companies by directly affecting their key performance indicators. Nowadays, in this era of big data, the information available about users and items has been continually updated and the application of traditional batch learning paradigms has become more restricted. In this sense, the current efforts in the recommendation field have concerned about this online environment and modeled their systems as a Multi-Armed Bandit (MAB) problem. Nevertheless, there is not a consensus about the best practices to design, perform, and evaluate the MAB implementations in the recommendation field. Thus, this work performs a systematic literature review (SLR) to shed light on this new topic. By inspecting 1327 articles published from the last twenty years (2000–2020), this work: (1) consolidates an updated picture of the main research conducted in this area so far; (2) highlights the most used concepts and methods, their core characteristics, and main limitations; and (3) evaluates the applicability of MAB-based recommendation approaches in some traditional RSs’ challenges, such as data sparsity, scalability, cold-start, and explainability. These discussions and analyzes also allow us to identify several gaps in the current literature, providing a strong guideline for future research.

[Reinforcement Learning to Rank in E-Commerce Search Engine](https://dl.acm.org/doi/pdf/10.1145/3219819.3219846)
Abstract: In E-commerce platforms such as Amazon and TaoBao, ranking
items in a search session is a typical multi-step decision-making
problem. Learning to rank (LTR) methods have been widely ap
plied to ranking problems. However, such methods often consider
different ranking steps in a session to be independent, which con
versely may be highly correlated to each other. For better utiliz
ing the correlation between different ranking steps, in this paper,
we propose to use reinforcement learning (RL) to learn an opti
mal ranking policy which maximizes the expected accumulative
rewards in a search session. Firstly, we formally define the concept
of search session Markov decision process (SSMDP) to formulate
the multi-step ranking problem. Secondly, we analyze the property
of SSMDP and theoretically prove the necessity of maximizing ac
cumulative rewards. Lastly, we propose a novel policy gradient al
gorithm for learning an optimal ranking policy, which is able to
deal with the problem of high reward variance and unbalanced
reward distribution of an SSMDP. Experiments are conducted in
simulation and TaoBao searchengine. The results demonstrate that
our algorithm performs much better than the state-of-the-art LTR
methods, with more than 40% and 30% growth of total transaction
amount in the simulation and the real application, respectively.