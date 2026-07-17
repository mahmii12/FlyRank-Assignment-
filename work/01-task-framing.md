# Task type
My search question — how do my queries/pages naturally group by topic or
intent — is a clustering task. It's unsupervised: there are no predefined
categories, so the goal is to let structure emerge from the data rather
than predict a known label.

# Method
Each query gets assigned to a cluster based on embedding similarity, so
semantically related queries end up grouped together even if they don't
share exact keywords.

# Success metric
I'll evaluate cluster quality using silhouette score, which measures how
tight each cluster is internally versus how well-separated it is from
other clusters. It's a standard, defensible metric for unsupervised
grouping — no labels required, and it directly checks whether the
clusters are meaningful rather than arbitrary.

# Validation
Beyond the numeric score, I'll manually review a sample of queries from
each cluster to confirm the groupings reflect real content gaps or
overlaps, not just noise. This also guards against overfitting — too
many tiny clusters would just be memorizing near-duplicate queries
instead of finding genuine intent groups.
