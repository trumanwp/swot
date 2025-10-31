# How to Submit SS Jain Subodh PG College to JetBrains/swot

## Current Status ✅

Your college has been **correctly added** to your fork of the swot repository:
- **File location:** `lib/domains/com/subodhpgcollege.txt`
- **Content:** `SS Jain Subodh PG College`
- **All tests passing:** ✅

## What Was Fixed

### Previous Mistakes (Now Corrected)
1. ❌ **PR #1:** Files placed in root directory instead of `lib/domains/`
2. ❌ **PR #2:** Attempted to merge 1,640 files from upstream (caused confusion)
3. ❌ **Incorrect file:** `lib/domains/in/subodhpgcollege.com` (wrong TLD and wrong extension)

### Current State (Correct) ✅
- ✅ File at: `lib/domains/com/subodhpgcollege.txt`
- ✅ Contains: `SS Jain Subodh PG College`
- ✅ All tests pass
- ✅ Follows repository structure guidelines

## How to Submit to JetBrains/swot (Upstream)

If you want to submit this to the official JetBrains/swot repository for approval:

### Step 1: Create a New Clean Branch

```bash
# Make sure you're on your master branch
git checkout master

# Create a new clean branch for upstream submission
git checkout -b add-subodh-college-upstream
```

### Step 2: Cherry-pick ONLY the College Addition

Since your current repository has many commits, you need to create a clean commit:

```bash
# Create the file
mkdir -p lib/domains/com
echo "SS Jain Subodh PG College" > lib/domains/com/subodhpgcollege.txt

# Add and commit
git add lib/domains/com/subodhpgcollege.txt
git commit -m "Add SS Jain Subodh PG College"
```

### Step 3: Push to Your Fork

```bash
git push origin add-subodh-college-upstream
```

### Step 4: Create Pull Request to JetBrains/swot

1. Go to https://github.com/JetBrains/swot
2. Click "New Pull Request"
3. Click "compare across forks"
4. Select:
   - **base repository:** JetBrains/swot
   - **base:** master
   - **head repository:** anacondy/swot
   - **compare:** add-subodh-college-upstream
5. Click "Create Pull Request"

### Step 5: Fill in the PR Description

Use this template for your PR description:

```markdown
### Summary
Add **SS Jain Subodh PG College** to the swot database to allow students to verify their academic status and access JetBrains' student benefits.

### Institution Details
- **Name:** SS Jain Subodh PG College
- **Location:** Tonk Road, Rambagh Circle, Jaipur, Rajasthan, India
- **Domain:** subodhpgcollege.com
- **Official Website:** https://www.subodhpgcollege.com/
- **Email:** admin@subodhpgcollege.com

### Accreditations
- **NAAC 'A++' Grade** - Highest accreditation in Northern India
- **NIRF Ranking:** 81st in India (2024 College Rankings by Ministry of Education)
- **UGC Recognition:** Declared "College of Excellence"
- **DBT STAR Status** - Department of Biotechnology, Government of India
- **Mentor College** - UGC Accreditation Framework
- **Model College** - Government of Rajasthan
- **Affiliations:** University of Rajasthan & Rajasthan Technical University

### IT Courses Offered
The college offers various IT-related programs including:
- B.Sc. Computer Science
- BCA (Bachelor of Computer Applications)
- M.Sc. Computer Science
- MCA (Master of Computer Applications)

All programs are long-term (2-3 years) and meet the repository requirements.

### Verification Links
- **College Website:** https://www.subodhpgcollege.com/
- **Course Details:** [Link to IT courses page on official website]
- **NAAC Certificate:** [Link if available]
- **NIRF Ranking:** [Link to government ranking]

### Notes
This is a clean, single-file addition following the repository structure guidelines. The domain `subodhpgcollege.com` is the official email domain for enrolled students.
```

## Important Notes

### Domain Verification
Make sure that:
1. `subodhpgcollege.com` is the actual domain used for student emails
2. You can provide proof (screenshot, documentation) that students receive emails with `@subodhpgcollege.com`
3. The domain is not shared with alumni or non-students

### If Domain is Different
If the actual student email domain is different (e.g., `student.subodhpgcollege.com` or `subodhpgcollege.in`), you should:
1. Use the correct domain
2. Place the file in the appropriate directory:
   - For `subodhpgcollege.in`: `lib/domains/in/subodhpgcollege.txt`
   - For `student.subodhpgcollege.com`: `lib/domains/com/subodhpgcollege/student.txt`

## Review Checklist

Before submitting to JetBrains/swot:
- [ ] Correct domain verified (subodhpgcollege.com)
- [ ] File placed in correct directory (lib/domains/com/subodhpgcollege.txt)
- [ ] File contains official college name
- [ ] Tests pass (`./gradlew test`)
- [ ] Only ONE file changed in the PR
- [ ] PR description includes all required information
- [ ] Can provide proof of domain ownership/usage

## Contact

If you have questions about the submission:
- Review the repository: https://github.com/JetBrains/swot
- Read CONTRIBUTING.md: https://github.com/JetBrains/swot/blob/master/CONTRIBUTING.md
- Check open PRs for examples: https://github.com/JetBrains/swot/pulls

## Timeline

JetBrains typically reviews PRs within:
- **Quick review (with all info):** 3-5 business days
- **Standard review:** 1-2 weeks
- **Complex cases:** 2-4 weeks

Providing all verification information upfront speeds up the process significantly.

---

**Your repository is now correctly structured and ready for submission!** 🎉
