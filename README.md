# AI-Ethics
Empirical evaluation of 8 LLMs using 5 domain-specific ethical dilemmas, to assess their behavior under different ethical principle prioritizations. By modifying the prioritization of ethical principles, we assess the effects on the decision outcomes, consistency and convergence of responses, within and across models and user runs. 

# Scope
We experimentally examine the effect of ethical prioritization in LLM behavior. We use ethical dilemmas spanning different sectors and context, to initially examine the behavior of LLMs based on their initial ethical training. Then without modifying their underlying ethical principles, we modify the prioritization among those principles to examine how this affects the consistency and convergence of responses within and across LLMs. 

## Selection and definition of ethical dilemmas 
Ethical dilemmas refer to situations where deciding what is right or wrong is non-obvious or even controversial. In addition, the morality of the decision may vary depending on the applied ethical framework; a decision considered ethically moral under deontological ethics, may be immoral under utilitarianism or virtue ethics. 
One of the most famous examples of ethical dilemmas is "the trolley problem". In its simplest form, a runaway trolley is headed towards five people, and the only way to save them is to press a button that will switch the trolley to a different track, eventually killing one person instead of five. Under consequentialism,  pressing the button is the most ethical decision, since it will benefit the most (maximizing beneficence) and harm less people (minimizing maleficence). However, under deontology, pressing the button is unethical, since it _actively_ violates the principle of treating all individuals as ends in themselves, with dignity and rights (fairness and justice are equal for all).

Besides their role in promoting critical thinking and revealing the complexities of ethics, arguments against such dilemmas emphasize inherent inconsistencies and the possibility of alternatives in realistic and less synthetic situations. Although this debate is beyond the scope of this work, for our purpose we have synthesized and applied 5 different dilemmas, based on the following criteria:

1) Describe scenarios _applicable in autonomous AI applications_, i.e., cases where AI components may take a decision even without human intervention.
2) The dilemmatic situation is _realistic_, i.e., can be reasonably expected to arise even in a small, but non-negligible, number of events.
3) _Avoid ethically-clear scenarios_, i.e., scenarios where an ethical principle would clearly have the highest priority (e.g., safety would clearly be prioritized against all other principles in a medical context). The scenarios were crafted to `neutralize' principles with expectedly high priority, so that none of the remaining principles is intuitively more important than the others.
4) Identify test scenarios in _different application contexts_, so that the examined LLMs could be tested for different context- and sector-specific prioritization.

# Synthesized ethical dilemmas
Based on the above criteria, five hypothetical scenarios were constructed to examine how LLMs treat ethical dilemmas. 
The first scenario is a variation of the trolley problem, where the safety impact is equal in both possible decisions. In addition, both parties (passenger and pedestrian) have violated a safety rule. The goal is to test how LLMs interpret concepts such as duty of care, implied contractual obligations, risk distribution, and moral accountability in autonomous vehicle decision-making.

The second scenario contrasts user privacy rights vs corporate sustainability in a high-impact cybersecurity incident, enabling analysis of AI responsibility, stakeholder prioritization and trade-offs in  cybersecurity. The goal is to examine whether the tested LLMs will prioritize customer privacy, corporate resilience, or strategic regulatory risk minimization.  

The third dilemma involves finance and in particular, AI-assisted investment systems. The goal is to examine the effect of ethical principles when clients' financial goals may contradict social responsibility or long-term ethical impact.

The fourth dilemma is from the health sector and examines the ethical concerns when patients' efficiency is set against hospitals' resource allocation. 

Finally, the fifth dilemma combines two sectors already examined in isolation in the previous scenarios:  autonomous vehicles and the health sector. However, it examines the effect of ethical principles in environmental optimization vs social equality and resource optimization. 
