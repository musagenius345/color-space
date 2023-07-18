<script>
import Button from './Button.svelte'
</script>

<div class="personal-info">
	<h2>Personal Information</h2>
	<p><strong>First Name:</strong> Samuel</p>
	<p><strong>Freelance:</strong> Available</p>
	<p><strong>Email:</strong> samuel@example.com</p>
	<p><strong>Languages:</strong> English, Arabic, German, Kiswahili</p>
	<p><strong>Phone:</strong> +1 (555) 123-4567</p>
	<Button --txt="black"
		><a href="/assets/docs/cv.pdf" download>
			<img class="icon" src="/icons/pdf.svg" width="40" height="30" href="icons/pdf.svg" />
			<p>Download CV</p>
		</a></Button>
</div>


  <style>
a{
  display: flex;
  gap: .9em;
  justify-content: space-around;
  padding-block: 1rem;
  color: var(--txt);
  text-decoration: none;
}
img{
max-width: 100%;
  align-self: center;
}
</style>
