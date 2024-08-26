<template>
    <div class="container-fluid p-0">
        <!-- Hero Section -->
        <div class="position-relative">
            <img src="https://hoec.com/wp-content/uploads/2023/08/jason-goodman-oalh2mojuuk-unsplash-scaled.jpg?id=4685" class="img-fluid w-100" alt="Careers"
                style="max-height: 300px; object-fit: cover;">
            <div class="position-absolute top-0 start-0 w-100 h-100 d-flex align-items-center"
                style="background-color: rgba(0,0,0,0.5);">
                <div class="container text-white">
                    <h1 class="display-4">CAREERS</h1>
                    <p class="lead">We encourage new ideas and professionalism mixed with teamwork to achieve your
                        career goals as well as making the customer satisfied.</p>
                </div>
            </div>
        </div>

        <!-- Application Form Section -->
        <div class="container my-5">
            <h2 class="mb-4">HELP US TO MOULD INNOVATION A LOT BETTER</h2>
            <p class="mb-4">We encourage new ideas and professionalism mixed with teamwork to achieve your career goals
                as well as making the customer satisfied. We constantly endeavour to create an environment in which our
                resources can take the liberty to perform well. We believe that our success as a company is the result
                of every team member's personal achievement. Come join us and explore a challenging career with perfect
                work culture.</p>

            <form @submit.prevent="submitForm">
                <div class="row g-3">
                    <div class="col-md-6">
                        <input v-model="form.applicantName" type="text" class="form-control"
                            placeholder="Applicant Name" required>
                    </div>
                    <div class="col-md-6">
                        <input v-model="form.mobileNo" type="tel" class="form-control" placeholder="Mobile No" required>
                    </div>
                    <div class="col-md-6">
                        <input v-model="form.alternateNo" type="tel" class="form-control" placeholder="Alternate No">
                    </div>
                    <div class="col-md-6">
                        <input v-model="form.emailId" type="email" class="form-control" placeholder="Email ID" required>
                    </div>
                    <div class="col-md-6">
                        <input v-model="form.dateOfBirth" type="date" class="form-control" placeholder="Date of Birth"
                            required>
                    </div>
                    <div class="col-md-6">
                        <select v-model="form.howDidYouHearAboutUs" class="form-select" required>
                            <option value="" disabled selected>How did you Hear About us?</option>
                            <option value="website">Website</option>
                            <option value="socialMedia">Social Media</option>
                            <option value="referral">Referral</option>
                        </select>
                    </div>
                    <div class="col-md-6">
                        <input v-model="form.academicQualifications" type="text" class="form-control"
                            placeholder="Academic Qualifications" required>
                    </div>
                    <div class="col-md-6">
                        <input v-model="form.totalYearsOfExperience" type="number" class="form-control"
                            placeholder="Total Years of Experience" required>
                    </div>
                    <div class="col-md-6">
                        <input v-model="form.currentSalary" type="number" class="form-control"
                            placeholder="Current Salary" required>
                    </div>
                    <div class="col-md-6">
                        <input v-model="form.expectedSalaryPackage" type="number" class="form-control"
                            placeholder="Expected Salary Package" required>
                    </div>
                    <div class="col-md-6">
                        <input v-model="form.joiningBy" type="date" class="form-control" placeholder="Joining By"
                            required>
                    </div>
                    <div class="col-md-6">
                        <select v-model="form.noticePeriod" class="form-select" required>
                            <option value="" disabled selected>Notice Period</option>
                            <option value="immediate">Immediate</option>
                            <option value="15days">15 Days</option>
                            <option value="30days">30 Days</option>
                        </select>
                    </div>
                    <div class="col-12">
                        <input v-model="form.presentCompanyAndDesignation" type="text" class="form-control"
                            placeholder="Present Company and Designation" required>
                    </div>
                    <div class="col-md-6">
                        <div class="mb-3">
                            <label for="resumeUpload" class="form-label">Upload Your Resume/CV in Word Format</label>
                            <input type="file" class="form-control" id="resumeUpload" accept=".doc,.docx"
                                @change="handleFileUpload">
                        </div>
                    </div>
                    <div class="col-12">
                        <button type="submit" class="btn btn-primary">Submit</button>
                    </div>
                </div>
            </form>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            form: {
                applicantName: '',
                mobileNo: '',
                alternateNo: '',
                emailId: '',
                dateOfBirth: '',
                howDidYouHearAboutUs: '',
                academicQualifications: '',
                totalYearsOfExperience: '',
                currentSalary: '',
                expectedSalaryPackage: '',
                joiningBy: '',
                noticePeriod: '',
                presentCompanyAndDesignation: '',
                resume: null
            }
        }
    },
    methods: {
        handleFileUpload(event) {
            this.form.resume = event.target.files[0]
        },
        submitForm() {
            // Here you would typically send the form data to your backend
            console.log(this.form)
            // You can add your form submission logic here
        }
    }
}
</script>