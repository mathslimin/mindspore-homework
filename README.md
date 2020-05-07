# mindspore-homework
mindspore作业

$python3.7 mnist_train.py

epoch: 10 step: 1845, loss is 0.0010520866
epoch: 10 step: 1846, loss is 0.00072324096
epoch: 10 step: 1847, loss is 0.011719422
epoch: 10 step: 1848, loss is 0.006982182
epoch: 10 step: 1849, loss is 0.0008360131
epoch: 10 step: 1850, loss is 0.00018114096
epoch: 10 step: 1851, loss is 0.00069725
epoch: 10 step: 1852, loss is 0.00069538114
epoch: 10 step: 1853, loss is 0.00062897865
epoch: 10 step: 1854, loss is 0.0009317736
epoch: 10 step: 1855, loss is 0.009880007
epoch: 10 step: 1856, loss is 0.0011836094
epoch: 10 step: 1857, loss is 0.0027219665
epoch: 10 step: 1858, loss is 0.0004850318
epoch: 10 step: 1859, loss is 0.20472533
epoch: 10 step: 1860, loss is 0.0009491106
epoch: 10 step: 1861, loss is 0.005131376
epoch: 10 step: 1862, loss is 0.0376039
epoch: 10 step: 1863, loss is 0.0025481358
epoch: 10 step: 1864, loss is 0.0011190445
epoch: 10 step: 1865, loss is 0.0035418263
epoch: 10 step: 1866, loss is 0.038394913
epoch: 10 step: 1867, loss is 0.0074735116
epoch: 10 step: 1868, loss is 0.0021618565
epoch: 10 step: 1869, loss is 0.00030577937
epoch: 10 step: 1870, loss is 0.11190292
epoch: 10 step: 1871, loss is 0.0037609215
epoch: 10 step: 1872, loss is 0.004227306
epoch: 10 step: 1873, loss is 0.0018360174
epoch: 10 step: 1874, loss is 0.14212744
epoch: 10 step: 1875, loss is 0.0051779193


 python3.7 mnist_attack_fgsm.py 
 
 
mnist_attack_fgsm.py:87: DeprecationWarning: time.clock has been deprecated in Python 3.3 and will be removed from Python 3.8: use time.perf_counter or time.process_time instead
  start_time = time.clock()
[ERROR] ME(3438,python):2020-05-07-23:11:49.929.959 [mindspore/ccsrc/device/cpu/cpu_session.cc:115] BuildKernel] Operator[SoftmaxCrossEntropyWithLogits] is not support.
Traceback (most recent call last):
  File "mnist_attack_fgsm.py", line 119, in <module>
    test_fast_gradient_sign_method()
  File "mnist_attack_fgsm.py", line 89, in test_fast_gradient_sign_method
    np.concatenate(test_labels), batch_size=32)
  File "/usr/local/lib/python3.7/dist-packages/mindarmour-0.2.0-py3.7.egg/mindarmour/attacks/attack.py", line 65, in batch_generate
    adv_x = self.generate(x_batch, y_batch)
  File "/usr/local/lib/python3.7/dist-packages/mindarmour-0.2.0-py3.7.egg/mindarmour/attacks/gradient_method.py", line 96, in generate
    gradient = self._gradient(inputs, labels)
  File "/usr/local/lib/python3.7/dist-packages/mindarmour-0.2.0-py3.7.egg/mindarmour/attacks/gradient_method.py", line 290, in _gradient
    out_grad = self._grad_all(Tensor(inputs), Tensor(labels), sens)
  File "/usr/local/lib/python3.7/dist-packages/mindspore/nn/cell.py", line 147, in __call__
    out = self.compile_and_run(*inputs)
  File "/usr/local/lib/python3.7/dist-packages/mindspore/nn/cell.py", line 301, in compile_and_run
    _, compile_flag = _executor.compile(self, *inputs, phase=self.phase)
  File "/usr/local/lib/python3.7/dist-packages/mindspore/common/api.py", line 363, in compile
    result = self._executor.compile(obj, args_list, phase, use_vm)
RuntimeError: mindspore/ccsrc/device/cpu/cpu_session.cc:115 BuildKernel] Operator[SoftmaxCrossEntropyWithLogits] is not support.
