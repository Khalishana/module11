## Reflection on Hello Minikube
1. Compare the application logs before and after you exposed it as a Service.
Try to open the app several times while the proxy into the Service is running.
What do you see in the logs? Does the number of logs increase each time you open the app? <br>
Jawab: Ya, terdapat perbedaan jumlah log setiap kali app dibuka. Setelah melakukan expose sebagai service, service tersebut dapat menerima request yang pernah dibuat pada log
2.  Notice that there are two versions of `kubectl get` invocation during this tutorial section.
The first does not have any option, while the latter has `-n` option with value set to
`kube-system`. What is the purpose of the `-n` option and why did the output not list the pods/services that you
explicitly created? <br>
Jawab: Penggunaan `-n` option pada versi kedua `kubectl get` menunjukkan bahwa service yang diinginkan berada pada namespace tersebut. Implementasi `-n` option ini berguna ketika terdapat banyak service berbeda yang memiliki nama yang sama di banyak namespace. Dengan penggunaan implementasi tersebut, perintah "GET" hanya difokuskan pada namespace spesifik yang diberikan tanda `-n` option saja