### 参考论文
[A Theoretically Grounded Application of Dropout in Recurrent Neural Networks](https://arxiv.org/pdf/1512.05287.pdf)

### TensorFlow中embedding_lookup的用法：
通俗来讲，首先创建一个参数矩阵，矩阵大小为(feature_size, embedding_size)，然后根据索引号，也就是feature_index，取出参数矩阵中下标为feature_index的元素组成一个一个矩阵返回。  

### category_featur与continuous_feature的Embedding做法
如果category_feature中取值少，就直接编号。多的话可采用hash处理，这样避免了过多的加法运算。  
category_feature与continuous_feature是一块进行embedding的，所以最终需要将feature_value的值与Embedding矩阵对应元素的值相乘，不同于矩阵相乘（tf.multiply），得到最终的Embedding Vector