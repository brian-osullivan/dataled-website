---
_schema: default
layout: page
permalink: /audit/
---
## What you’ll get

**Personalized video audit:** A 10-15 minute screen recording highlighting specific issues and opportunities.

**Written summary:** Key findings and prioritized recommendations you can share with your team.

## What makes this different

Unlike generic audits that give you a checklist of best practices, I provide specific recommendations based on your business model, target audience, and current performance. Every recommendation is actionable and prioritized by potential impact.

**Questions?** Email me at [brian@dataled.co](mailto:brian@dataled.co)

---

&nbsp;

<form id="contact-form">
  <div>
    <label for="firstname">First Name</label>
    <input type="text" id="firstname" name="firstname" required="" />
  </div>
  <div>
    <label for="lastname">Last Name</label>
    <input type="text" id="lastname" name="lastname" required="" />
  </div>
  <div>
    <label for="email">Email</label>
    <input type="email" id="email" name="email" required="" />
  </div>
  <button type="submit">Submit</button>
</form>

&nbsp;

<script>
document.getElementById('contact-form').addEventListener('submit', function(e) {
  e.preventDefault();

  const formData = {
    fields: [
      { name: "firstname", value: document.querySelector('[name="firstname"]').value },
      { name: "lastname", value: document.querySelector('[name="lastname"]').value },
      { name: "email", value: document.querySelector('[name="email"]').value }    ]
  };

  fetch('https://api.hsforms.com/submissions/v3/integration/submit/147458409/b9f9ecaa-70dd-4126-a0ab-a92dbc1def3d', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify(formData)
  })
  .then(response => response.json())
  .then(data => {
    alert('Thanks! We\'ll be in touch soon.');
    this.reset();
  })
  .catch(error => {
    alert('Something went wrong. Please try again.');
  });
});
</script>

&nbsp;

&nbsp;