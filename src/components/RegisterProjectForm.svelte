<script lang="ts">
 let projectName: string = '';
 let projectDescription = '';
 let projectRequirements = '';
 let estimatedDuration = '';

 function handleSubmit() {
    console.log('Project Name:', projectName);
    console.log('Project Description:', projectDescription);
    console.log('Project Requirements:', projectRequirements);
    console.log('Estimated Duration:', estimatedDuration);
 }
</script>

<form on:submit|preventDefault={handleSubmit}>
    <div>
        <label for="projectName">Project Name:</label>
        <input type="text" id="projectName" bind:value={projectName} required />
    </div>
    <div>
        <label for="projectDescription">Project Description:</label>
        <textarea id="projectDescription" bind:value={projectDescription} required></textarea>
    </div>
    <div>
        <label for="hardSpecifications">Hard Specifications:</label>
        <textarea id="hardSpecifications" bind:value={projectRequirements}></textarea>
    </div>
    <div>
        <label for="estimatedDuration">Estimated Duration:</label>
        <input type="time" id="estimatedDuration" bind:value={estimatedDuration} />
    </div>
    <button type="submit">Register Project</button>
</form>

<style>
 /* General form styles */
 form {
     max-width: 500px;
     margin: 0 auto;
     padding: 20px;
     background-color: #f5f5f5;
     border: 1px solid #ddd;
     border-radius: 5px;
     box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
 }

 /* Input field styles */
 input[type="text"],
 textarea,
 input[type="time"] {
     width: 100%;
     padding: 10px;
     margin-bottom: 15px;
     border: 1px solid #ccc;
     border-radius: 4px;
     box-sizing: border-box;
     font-size: 16px;
 }

 /* Textarea styles */
 textarea {
     height: 150px;
     resize: vertical;
 }

 /* Submit button styles */
 button[type="submit"] {
     background-color: #4CAF50;
     color: white;
     padding: 12px 20px;
     border: none;
     border-radius: 4px;
     cursor: pointer;
     font-size: 16px;
 }

 button[type="submit"]:hover {
     background-color: #45a049;
 }

 /* Field label styles */
 label {
     display: block;
     font-weight: bold;
     margin-bottom: 5px;
 }

 /* Field container styles */
 div {
     margin-bottom: 20px;
 }
</style>
