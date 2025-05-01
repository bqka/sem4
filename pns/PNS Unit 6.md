![[Pasted image 20250430030033.png]]
![[Pasted image 20250501020017.png]]

![[Pasted image 20250501020701.png]]

Values for testing
![[Pasted image 20250501025435.png]]
### **1. Z-Test (Large Samples)**
- **Single Mean:**
  $$Z = \frac{\overline{X} - \mu_0}{\sigma / \sqrt{n}}$$

- **Difference of Two Means:**
  $$Z = \frac{(\overline{X}_1 - \overline{X}_2) - (\mu_1 - \mu_2)}{\sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}}}$$

- **Single Proportion:**
  $$Z = \frac{p - P_0}{\sqrt{\frac{P_0 (1 - P_0)}{n}}}$$

- **Difference of Two Proportions:**
  $$Z = \frac{(p_1 - p_2)}{\sqrt{\overline{p} (1 - \overline{p}) \left(\frac{1}{n_1} + \frac{1}{n_2}\right)}}$$
  where $$\overline{p} = \frac{n_1 p_1 + n_2 p_2}{n_1 + n_2}$$

---

### **2. t-Test (Small Samples)**
- **Single Mean (σ unknown):**
  $$t = \frac{\overline{X} - \mu_0}{s / \sqrt{n}} \quad \text{df} = n-1$$

- **Difference of Two Means (Independent Samples):**
  $$t = \frac{(\overline{X}_1 - \overline{X}_2)}{\sqrt{s_p^2 \left(\frac{1}{n_1} + \frac{1}{n_2}\right)}} \quad \text{df} = n_1 + n_2 - 2$$
  where $$s_p^2 = \frac{(n_1 - 1)s_1^2 + (n_2 - 1)s_2^2}{n_1 + n_2 - 2}$$

- **Paired t-Test:**
  $$t = \frac{\overline{d}}{s_d / \sqrt{n}} \quad \text{df} = n-1$$

---

### **3. F-Test (Variance Equality)**
$$F = \frac{s_1^2}{s_2^2} \quad \text{df}_1 = n_1 - 1, \ \text{df}_2 = n_2 - 1$$

---

### **4. Chi-Square Test (Goodness of Fit)**
$$\chi^2 = \sum \frac{(f_i - e_i)^2}{e_i} \quad \text{df} = k - 1$$

fi -> frequency
ei -> expected frequency
expected frequency = sum of freq/n
### **Key Terms:**
- **Type I Error:** $$\alpha = P(\text{Reject } H_0 \mid H_0 \text{ true})$$
- **Type II Error:** $$\beta = P(\text{Accept } H_0 \mid H_0 \text{ false})$$
- **Power:** $$1 - \beta$$

---

### **Critical Values:**
- Reject \(H_0\) if:
  - For Z/t-tests: $$| \text{Test Statistic} | > \text{Critical Value}$$
  - For F/χ²-tests: $$\text{Test Statistic} > \text{Critical Value}$$
![[Pasted image 20250501041756.png]]