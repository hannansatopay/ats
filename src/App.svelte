<script>
  import svelteLogo from './assets/svelte.svg'
  import viteLogo from '/vite.svg'
  import Counter from './lib/Counter.svelte'
</script>

<main>
   <h1>Internship/Job Application Form</h1>
    <form action="submit.php" method="POST">
        <h2>Opportunity Type</h2>
        <input type="radio" id="internship" name="opportunityType" value="internship" required>
        <label for="internship">Internship</label>
        <input type="radio" id="fresher" name="opportunityType" value="fresher" required>
        <label for="fresher">Fresher Job</label>

        <h2>Internship Details</h2>
        <label for="internshipProfile">Internship Profile:</label>
        <input type="text" id="internshipProfile" name="internshipProfile" required>

        <label for="skillsRequired">Skills Required:</label>
        <input type="text" id="skillsRequired" name="skillsRequired">

        <h3>Internship Type:</h3>
        <input type="radio" id="inOffice" name="internshipType" value="inOffice" required>
        <label for="inOffice">In-Office/Hybrid</label>
        <input type="radio" id="remote" name="internshipType" value="remote" required>
        <label for="remote">Remote</label>

        <label for="openings">Number of Openings:</label>
        <input type="number" id="openings" name="openings" required>

        <h3>Internship Start Date:</h3>
        <input type="radio" id="immediately" name="startDate" value="immediately" required>
        <label for="immediately">Immediately (within next 30 days)</label>
        <input type="radio" id="later" name="startDate" value="later" required>
        <label for="later">Later</label>

        <label for="duration">Internship Duration:</label>
        <select id="duration" name="duration" required>
            <option value="" disabled selected>Choose Duration</option>
            <option value="1">1 month</option>
            <option value="2">2 months</option>
            <option value="3">3 months</option>
        </select>

        <label for="responsibilities">Intern's Responsibilities:</label>
        <textarea id="responsibilities" name="responsibilities" required></textarea>

        <input type="checkbox" id="allowWomen" name="allowWomen" value="yes">
        <label for="allowWomen">Allow applications from women also who are willing to start/restart their career.</label>

        <p>Know More</p>

        <h2>Stipend &amp; Perks</h2>
        <h3>Stipend:</h3>
        <input type="radio" id="fixed" name="stipend" value="fixed" required>
        <label for="fixed">Fixed</label>
        <input type="radio" id="negotiable" name="stipend" value="negotiable" required>
        <label for="negotiable">Negotiable</label>
        <input type="radio" id="performanceBased" name="stipend" value="performanceBased" required>
        <label for="performanceBased">Performance-based</label>
        <input type="radio" id="unpaid" name="stipend" value="unpaid" required>
        <label for="unpaid">Unpaid</label>

        <h3>Perks:</h3>
        <div>
            <input type="checkbox" id="certificate" name="perks[]" value="certificate">
            <label for="certificate">Certificate</label><br>
            <input type="checkbox" id="flexibleHours" name="perks[]" value="flexibleHours">
            <label for="flexibleHours">Flexible Work Hours</label><br>
            <input type="checkbox" id="informalDressCode" name="perks[]" value="informalDressCode">
            <label for="informalDressCode">Informal Dress Code</label><br>
        </div>
        <div>
            <input type="checkbox" id="letterOfRecommendation" name="perks[]" value="letterOfRecommendation">
            <label for="letterOfRecommendation">Letter of Recommendation</label><br>
            <input type="checkbox" id="fiveDaysWeek" name="perks[]" value="fiveDaysWeek">
            <label for="fiveDaysWeek">5 Days a Week</label><br>
            <input type="checkbox" id="freeSnacksBeverages" name="perks[]" value="freeSnacksBeverages">
            <label for="freeSnacksBeverages">Free Snacks &amp; Beverages</label><br>
        </div>

        <h2>Does this internship come with a pre-placement offer (PPO)?</h2>
        <input type="text" id="prePlacementOffer" name="prePlacementOffer" placeholder="Optional">

        <h2>Cover Letter, Availability &amp; Assessment Question</h2>
        <label for="coverLetter">Cover Letter:</label>
        <textarea id="coverLetter" name="coverLetter"></textarea>

        <label for="availabilityQuestion">Availability &amp; Assessment Question:</label>
        <textarea id="availabilityQuestion" name="availabilityQuestion"></textarea>

        <p>+ Add assessment question</p>

        <h2>Alternate Mobile Number</h2>
        <label for="mobileNumber">Mobile Number:</label>
        <input type="tel" id="mobileNumber" name="mobileNumber" required>

        <h2>Post Internship</h2>
        <input type="button" value="Save Draft">
        <input type="submit" value="Post Internship">
    </form>
</main>

<style>
  .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
    transition: filter 300ms;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.svelte:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }
  .read-the-docs {
    color: #888;
  }
</style>
