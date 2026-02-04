# Research Notes on Reinforcement Learning and Recommendation Systems

## 1. Deep Reinforcement Learning for Recommender Systems

**Citation:** [1] Isshu Munemasa, Yuta Tomomatsu, K. Hayashi, and T. Takagi, "Deep reinforcement learning for recommender systems," Mar. 2018, doi: https://doi.org/10.1109/icoiact.2018.8350761.

**Source:** [IEEE Xplore](https://ieeexplore.ieee.org/abstract/document/8350761)

**Abstract:**

Services that introduce stores to users on the Internet are increasing in recent years. Each service conducts thorough analyses in order to display stores matching each user's preferences. In the field of recommendation, collaborative filtering performs well when there is sufficient click information from users. Generally, when building a user-item matrix, data sparseness becomes a problem. It is especially difficult to handle new users. When sufficient data cannot be obtained, a multi-armed bandit algorithm is applied. Bandit algorithms advance learning by testing each of a variety of options sufficiently and obtaining rewards (i.e. feedback). It is practically impossible to learn everything when the number of items to be learned periodically increases. The problem of having to collect sufficient data for a new user of a service is the same as the problem that collaborative filtering faces. In order to solve this problem, we propose a recommender system based on deep reinforcement learning. In deep reinforcement learning, a multilayer neural network is used to update the value function.

---

## 2. Survey on Reinforcement Learning for Recommender Systems

**Citation:** [1] Y. Lin et al., "A Survey on Reinforcement Learning for Recommender Systems," IEEE Transactions on Neural Networks and Learning Systems, pp. 1–21, 2023, doi: https://doi.org/10.1109/TNNLS.2023.3280161.

**Source:** [IEEE Xplore](https://ieeexplore.ieee.org/abstract/document/10144689)

**Abstract:**

Recommender systems have been widely applied in different real-life scenarios to help us find useful information. In particular, reinforcement learning (RL)-based recommender systems have become an emerging research topic in recent years, owing to the interactive nature and autonomous learning ability. Empirical results show that RL-based recommendation methods often surpass supervised learning methods. Nevertheless, there are various challenges in applying RL in recommender systems. To understand the challenges and relevant solutions, there should be a reference for researchers and practitioners working on RL-based recommender systems. To this end, we first provide a thorough overview, comparisons, and summarization of RL approaches applied in four typical recommendation scenarios, including interactive recommendation, conversational recommendation, sequential recommendation, and explainable recommendation. Furthermore, we systematically analyze the challenges and relevant solutions on the basis of existing literature. Finally, under discussion for open issues of RL and its limitations of recommender systems, we highlight some potential research directions in this field.

---

## 3. Multi-Armed Bandits in Recommendation Systems

**Citation:** [1] N. Silva, H. Werneck, T. Silva, A. C. M. Pereira, and L. Rocha, "Multi-Armed Bandits in Recommendation Systems: A survey of the state-of-the-art and future directions," Expert Systems with Applications, vol. 197, p. 116669, Jul. 2022, doi: https://doi.org/10.1016/j.eswa.2022.116669.

**Source:** [ScienceDirect](https://www.sciencedirect.com/science/article/abs/pii/S0957417422001543?fr=RR-2&ref=pdf_download&rr=9c63b7ceef068cb8)

**Abstract:**

Recommender Systems (RSs) have assumed a crucial role in several digital companies by directly affecting their key performance indicators. Nowadays, in this era of big data, the information available about users and items has been continually updated and the application of traditional batch learning paradigms has become more restricted. In this sense, the current efforts in the recommendation field have concerned about this online environment and modeled their systems as a Multi-Armed Bandit (MAB) problem. Nevertheless, there is not a consensus about the best practices to design, perform, and evaluate the MAB implementations in the recommendation field. Thus, this work performs a systematic literature review (SLR) to shed light on this new topic. By inspecting 1327 articles published from the last twenty years (2000–2020), this work: (1) consolidates an updated picture of the main research conducted in this area so far; (2) highlights the most used concepts and methods, their core characteristics, and main limitations; and (3) evaluates the applicability of MAB-based recommendation approaches in some traditional RSs' challenges, such as data sparsity, scalability, cold-start, and explainability. These discussions and analyzes also allow us to identify several gaps in the current literature, providing a strong guideline for future research.

### Personal Analysis:

What they are doing is reading articles plublished from 2000 - 2020 to give an update on what is being researched. Finding common concepts, methods, and main limitations. And lastly, talking about how applicable MAB algorithms are to recommendation system challenges, like data sparsity, cold-start and explainability, and privacy.

### Key Quote:

"While exploitation just means pull arms with the highest rewards in the past, maximizing the system short-term reward, exploration is achieved by recommending other arms to improve the knowledge available about users and items to maximize the system long-term reward (Sanz-Cruzado et al., 2019, Zhao et al., 2013)."

### Problem and Main Contribution:

However, even with this growing number of new publications available, there is no work that aims to map the main advances in the area, explain the main concepts, and clarify the best practices. Therefore, this work performs a systematic literature review (SLR) about MAB in the recommendation field to achieve three main goals:

1. Provide a summary overview of the most important research in this area;
2. Highlight the most popular concepts and methods, their core characteristics, and their main limitations to provide future directions of the field to guide the next research questions;
3. Discuss the applicability of MAB-based recommendation approaches in some traditional RSs' challenges, such as the data sparsity, scalability, cold-start, privacy, and explainability.

### Methodology Note:

"While the first step performs a short reading by analyzing titles, year, conference, and abstract, the second one performs a more complete analysis by reading the introduction, experimentation, and conclusion of each work."

### Personal Notes:

I was limited to the free access of this paper which included the full introduction to the paper but only snippets of the read of the study. From what I was able to read, there wasn't any information on how different MAB models are implemented or what datasets were used. I didn't read about any techinical things, just a high overview of where things in the MAB are current at.

---

## 4. Reinforcement Learning to Rank in E-Commerce Search Engine

**Citation:** [1] Y. Hu, Q. Da, A. Zeng, Y. Yu, and Y. Xu, "Reinforcement Learning to Rank in E-Commerce Search Engine," Proceedings of the 24th ACM SIGKDD International Conference on Knowledge Discovery & Data Mining, Jul. 2018, doi: https://doi.org/10.1145/3219819.3219846.

**Source:** [ACM Digital Library](https://dl.acm.org/doi/pdf/10.1145/3219819.3219846)

**Abstract:**

In E-commerce platforms such as Amazon and TaoBao, ranking items in a search session is a typical multi-step decision-making problem. Learning to rank (LTR) methods have been widely applied to ranking problems. However, such methods often consider different ranking steps in a session to be independent, which conversely may be highly correlated to each other. For better utilizing the correlation between different ranking steps, in this paper, we propose to use reinforcement learning (RL) to learn an optimal ranking policy which maximizes the expected accumulative rewards in a search session. Firstly, we formally define the concept of search session Markov decision process (SSMDP) to formulate the multi-step ranking problem. Secondly, we analyze the property of SSMDP and theoretically prove the necessity of maximizing accumulative rewards. Lastly, we propose a novel policy gradient algorithm for learning an optimal ranking policy, which is able to deal with the problem of high reward variance and unbalanced reward distribution of an SSMDP. Experiments are conducted in simulation and TaoBao searchengine. The results demonstrate that our algorithm performs much better than the state-of-the-art LTR methods, with more than 40% and 30% growth of total transaction amount in the simulation and the real application, respectively.

---

## 5. Bandit Algorithms: A Comprehensive Review

**Citation:** [1] Alexandre Letard, N. Gutowski, O. Camp, and Tassadit Amghar, "Bandit algorithms: A comprehensive review and their dynamic selection from a portfolio for multicriteria top-k recommendation," Expert Systems with Applications, vol. 246, pp. 123151–123151, Jul. 2024, doi: https://doi.org/10.1016/j.eswa.2024.123151.

**Source:** [ScienceDirect](https://www.sciencedirect.com/science/article/abs/pii/S0957417424000162)

**Abstract:**

This paper discusses the use of portfolio approaches based on bandit algorithms to optimize multicriteria decision-making in recommender systems (accuracy and diversity). While previous research has primarily focused on single-item recommendations, this study extends the research to consider the recommendation of several items per iteration. Two methods, Multiple-play Gorthaur and Budgeted-Gorthaur, are proposed to solve the algorithm selection problem and their performances on real-world datasets are compared. Both methods provide a generalization of the Gorthaur method, which enables it to operate with any Multi-Armed Bandit (MAB) and Contextual Multi-Armed Bandit (CMAB) algorithm as meta-algorithm in a multi-item recommendation scenario. For Multiple-play Gorthaur, an empirical evaluation shows that the use of Thompson Sampling for algorithm selection (Gorthaur-TS) yields better results than the original EXP3 method (Gorthaur-EXP3) and the exclusive use of the optimal algorithm in the portfolio in contextual recommendation problems. Additionally, the paper includes a theoretical regret analysis based on the TS sketch proof applied for this variant of the method. Concerning Budgeted-Gorthaur, experiments show that it allows more flexibility to achieve a suitable trade-off between criteria and a broader coverage of the Pareto set of solutions, overcoming a natural limit of "a-priori" methods. Finally, this paper provides a detailed review, including pseudocodes and theoretical bounds, for all the fundamental MAB and CMAB algorithms used in this study.

---

## 6. Recommendation Systems: Current Development and Future Research Challenges

**Citation:** [1] M. Marcuzzo, A. Zangari, A. Albarelli, and A. Gasparetto, "Recommendation Systems: An Insight Into Current Development and Future Research Challenges," IEEE Access, vol. 10, pp. 86578–86623, 2022, doi: https://doi.org/10.1109/access.2022.3194536.

**Source:** [IEEE Xplore](https://ieeexplore.ieee.org/document/9843966)

**Abstract:**

Research on recommendation systems is swiftly producing an abundance of novel methods, constantly challenging the current state-of-the-art. Inspired by advancements in many related fields, like Natural Language Processing and Computer Vision, many hybrid approaches based on deep learning are being proposed, making solid improvements over traditional methods. On the downside, this flurry of research activity, often focused on improving over a small number of baselines, makes it hard to identify reference methods and standardized evaluation protocols. Furthermore, the traditional categorization of recommendation systems into content-based, collaborative filtering and hybrid systems lacks the informativeness it once had. With this work, we provide a gentle introduction to recommendation systems, describing the task they are designed to solve and the challenges faced in research. Building on previous work, an extension to the standard taxonomy is presented, to better reflect the latest research trends, including the diverse use of content and temporal information. To ease the approach toward the technical methodologies recently proposed in this field, we review several representative methods selected primarily from top conferences and systematically describe their goals and novelty. We formalize the main evaluation metrics adopted by researchers and identify the most commonly used benchmarks. Lastly, we discuss issues in current research practices by analyzing experimental results reported on three popular datasets.