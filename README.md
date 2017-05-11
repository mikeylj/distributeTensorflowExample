# distributeTensorflowExample
分布式Tensorflow运行示例
    y = weight * x + biasis
简介:
    This is a most simple example for distributed tensorflow.

    The task is to estimate the paramters of the formula : Y = 2 * X + 10

    the paramter weight is the number 2,

    the paramter biasis is the number 10.
运行方式:
    server:

        CUDA_VISIBLE_DEVICES='' python distribute.py --ps_hosts=192.168.100.42:2222 --worker_hosts=192.168.100.42:2224,192.168.100.253:2225 --job_name=ps --task_index=0



    worker server:

        CUDA_VISIBLE_DEVICES=0 python distribute.py --ps_hosts=192.168.100.42:2222 --worker_hosts=192.168.100.42:2224,192.168.100.253:2225 --job_name=worker --task_index=0

        CUDA_VISIBLE_DEVICES=0 python distribute.py --ps_hosts=192.168.100.42:2222 --worker_hosts=192.168.100.42:2224,192.168.100.253:2225 --job_name=worker --task_index=1








