# Link-analysis-and-Information-Cascades

In this section, we'll then move to link analysis and implement a simplified versions of the PageRank and HITS algorithm to find the more important nodes in the network. Finally, we'll compare our PageRank scores with networkx Pagerank scores and scores from the HITS algorithm.

Personalized PageRank algorithm is an extension of the PageRank algorithm where the teleportation set of the random walker is restricted to a set  𝑆  of nodes. Given the teleportation set  𝑆  of nodes, we can calculate the stationary distribution of a random walker visiting all nodes in the graph. This distribution over all nodes with respect to  𝑆  is called the Personalized PageRank Distribution. This is represented as vector  𝑃𝑃𝑅𝐷(∗|𝑆) .

Assume two disjoint teleportation sets  𝑆1  and  𝑆2 , such that  𝑆1∩𝑆2=𝜙 . The Personalized PageRank Distribution of the set  𝑆1∪𝑆2  can be calculated as  𝑃𝑃𝑅𝐷(∗|𝑆1∪𝑆2)=𝑃𝑃𝑅𝐷(∗|𝑆1)+𝑃𝑃𝑅𝐷(∗|𝑆2) . This is because the distributions are stationary and the contributions of nodes in the two sets is complementary.

Suppose you have already calculated the Personalized PageRank Distribution vectors for various set teleportation sets  𝑆 :

𝑃𝑃𝑅𝐷(∗|{1,2,3})  for  𝑆={1,2,3} 
𝑃𝑃𝑅𝐷(∗|{3,4,5})  for  𝑆={3,4,5} 
𝑃𝑃𝑅𝐷(∗|{1,4,5})  for  𝑆={1,4,5} 
𝑃𝑃𝑅𝐷(∗|{1})  for  𝑆={1}
