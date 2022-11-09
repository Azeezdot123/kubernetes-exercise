Create a network policy to allow traffic from the Internal application only to the **payroll-service** and **db-service**.

Use the spec given below. You might want to enable ingress traffic to the pod to test your rules in the UI:


* Policy Name: **internal-policy**

* Policy Type: **Egress**

* Egress Allow: **payroll**

* Payroll Port: **8080**

* Egress Allow: **mysql**

* MySQL Port: **3306**