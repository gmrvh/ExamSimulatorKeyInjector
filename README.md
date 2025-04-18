Intercepts HTTP requests to the exam simulator's server, checks if any known encrypted keys exist in the request body, and injects a pre-defined exam key as the response. Therefore bypassing the VCE's copy protection.

###How it Works
Monitors HTTP traffic using mitmproxy.
If the request URL matches the specified Avanset license endpoint:
Iterates through a set of known keys. (We must have the exam key from an activated device)
if a key is found to match the initial request body, mitmproxy responds directly with a mapped value, simulating a valid exam key response.
