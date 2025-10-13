# Robust Q Learning under corrupted rewards
Recently, there has been a growing interest in understanding the non-asymptotic behavior of model-free reinforcement learning algorithms. Despite this focus, the performance of these algorithms in non-ideal settings, such as those with corrupted rewards, remains poorly understood. Addressing this gap, we examine the robustness of the well-known Q-learning algorithm under a strong-contamination attack model, where an adversary can arbitrarily perturb a small fraction of observed rewards. We first demonstrate that such attacks can lead to unbounded errors in the standard Q-learning algorithm. To counter this, we propose a novel robust synchronous Q-learning algorithm that leverages historical reward data to construct robust empirical Bellman operators at each time step. We further establish a finite-time convergence rate for our algorithm, which matches the best-known bounds for Q-learning in the absence of attacks, up to a small unavoidable error $O(\varepsilon)$ that scales with the adversarial corruption fraction $\varepsilon$.

## Citation

```bash
@INPROCEEDINGS{10885945,
  author={Maity, Sreejeet and Mitra, Aritra},
  booktitle={2024 IEEE 63rd Conference on Decision and Control (CDC)}, 
  title={Robust Q-Learning under Corrupted Rewards}, 
  year={2024},
  volume={},
  number={},
  pages={1181-1186},
  keywords={Lower bound;Analytical models;Q-learning;Approximation algorithms;Robustness;Function approximation;Surges;Convergence},
  doi={10.1109/CDC56724.2024.10885945}}

```

## Figures

Test Case:  Consider the MDP depicted in the figure. In the absence of attacks, state 1 yields a reward of $d$ when taking action $a = L$ and a reward of $-d$ for action $a = R$, where $d > 0$. States 2 and 3 provide a reward of 1, while states 4 and 5 provide a reward of 0. Under a Huber attack model, the rewards in state $s = 1$ are perturbed: for the state-action pair $(1, L)$, the reward is $d$ with probability $1-\varepsilon$ and $-C$ with probability $\varepsilon$; for $(1, R)$, the reward is $-d$ with probability $1-\varepsilon$ and $C$ with probability $\varepsilon$. The corruption signal $C$ is defined as $\left((2-\varepsilon)d + \kappa\right) \varepsilon^{-1}$, where $\kappa > 0$ is a tunable parameter. The error norm $\lVert Q_t - Q^* \rVert_\infty$ is plotted for both the Vanilla Q-Learning Algorithm under corruption with $\varepsilon = 0.01$ (red) and our proposed $\varepsilon$-Robust TD Learning Algorithm under the same corruption level (blue), highlighting the significant improvement of our approach. C and d are problem-specific, and user can manipulate these value, to generate many test cases. Also, with a small change in the provided code, one can expect to carry out the numerical experiment with different MDPs.

This numerical simulation aligns with our proven result, accepted for presentation, and publication at the 63rd IEEE Conference on Decision and Control.
<table>
  <tr>
    <td>
      <img src="https://github.com/sreejeetm1729/Robust_Reinforcement_Learning_CDC/blob/main/Figures%20and%20Plots" style="width:760px">
    </td>
  </tr>
<tr>
  <td>
    <img src="https://github.com/sreejeetm1729/Robust-Q-Learning-under-Corrupted-Rewards/blob/main/Q_learning_convergence_plot_with_different_epsilons.png" style="width:380px">
    <img src="https://github.com/sreejeetm1729/Robust-Q-Learning-under-Corrupted-Rewards/blob/main/Robust_Q_learning_convergence_plot_with_different_epsilons.png" style="width:380px">
 </td>
</tr>
