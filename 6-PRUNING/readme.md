<table>
  <tr>
    <td  width="130">
      <a href="https://amzn.to/4eanT1g">
        <img src="https://github.com/peremartra/Large-Language-Model-Notebooks-Course/blob/main/img/Large_Language_Models_Projects_Book.jpg" height="160" width="104">
      </a>
    </td>
    <td>
      <p>
        This is the unofficial repository for the book: 
        <a href="https://amzn.to/4eanT1g"> <b>Large Language Models:</b> Apply and Implement Strategies for Large Language Models</a> (Apress).
        The book is based on the content of this repository, but the notebooks are being updated, and I am incorporating new examples and chapters.
        If you are looking for the official repository for the book, with the original notebooks, you should visit the 
        <a href="https://github.com/Apress/Large-Language-Models-Projects">Apress repository</a>, where you can find all the notebooks in their original format as they appear in the book. Buy it at: <a href="https://amzn.to/3Bq2zqs">[Amazon]</a> <a href="https://link.springer.com/book/10.1007/979-8-8688-0515-8">[Springer]</a>
      </p>
    </td>
  </tr>
</table>

# Pruning Techniques for Large Language Models

Pruning is a crucial optimization technique in machine learning, particularly for large language models (LLMs). It involves reducing the size and complexity of a model by eliminating less important components—such as neurons, layers, or weights, while maintaining most of the model’s performance. Pruning helps to make models more efficient, reducing their computational and memory requirements, which is especially important when deploying models on resource-constrained environments like mobile devices or edge servers.

One of the great advantages of pruning compared to other techniques like quantization is that when selecting parts of the model to remove, you can choose those that contribute less to the model’s output, depending on the intended use.

## Structured Width Pruning: Eliminating Less Important Neurons from Feedforward Layers.
In this type of pruning, the neurons that contribute least to the model's output are identified and removed. It is crucial to know or have access to the model's structure, as the pruning process is not applied to all layers. Depending on the need, specific layers are selected for pruning.

In the first notebook, the pruning process will be applied to the feedforward layers of a distilGPT2 model. This means the model will have reduced weights in those specific layers. The neurons to prune are selected based on their importance scores, which we compute using the L1 norm of their weights. It is a simple aproach, for this first example, that can be used when you want to create a Pruned Model that mimics the Base model in all the areas. 

By altering the model's structure, a new configuration file must be created to ensure it works correctly with the `transformers` library.

| [Notebook](https://github.com/peremartra/Large-Language-Model-Notebooks-Course/blob/main/6-PRUNING/6_1_pruning_structured_l1_diltilgpt2.ipynb)
| --- |




