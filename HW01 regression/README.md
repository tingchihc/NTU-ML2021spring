## note ##

To function that can direct PyTorch operators to select deterministic algorithms when available, and to throw a runtime error if an operation may result in nondeterministic behavior.  
`torch.backends.cudnn.deterministic = True`

Disabling the benchmarking feature with function, causing cuDNN to deterministically select an algorithm, possibly at the cost of reduced performance.  
`torch.backends.cudnn.benchmark = False`
