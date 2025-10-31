# Understanding the "Fraud" Tag Issue - Explanation

## What Happened?

Your PR did **NOT** get a "fraud" tag. Let me explain what actually happened:

### The Real Issue: File Placement Mistake

When you submitted your first PR (#1), you accidentally placed files in the **wrong location**:
- ❌ You added: `subodhpgcollege.txt` in the **root directory** of the repository
- ❌ You also added: `file.zip` in the **root directory**
- ✅ Should have been: `lib/domains/com/subodhpgcollege.txt`

### Why This Was Wrong

The swot repository has a specific structure for domains:
- Each educational domain must be in `lib/domains/` directory
- The path should follow the domain structure reversed: `lib/domains/{TLD}/{DOMAIN_NAME}.txt`
- For `subodhpgcollege.com`, the correct path is: `lib/domains/com/subodhpgcollege.txt`

## Understanding PR #2

Your second PR (#2) titled "Add SS Jain Subodh PG College to the dataset" was attempting to merge changes from **JetBrains/swot master branch** (the upstream repository) into your fork. This is why:

1. The PR shows 1,640 files changed
2. It includes many unrelated changes to the swot database
3. It updates the `lib/domains/abused.txt` file with 1,402 lines

The "abused.txt" file is NOT a fraud list for your college. It's a list maintained by JetBrains of email domains that have been abused in the past by people trying to fraudulently get free student licenses. Your college is **NOT** on this list.

## The Confusion About "Fraud"

You mentioned seeing the word "fraud" but this likely came from:
1. The filename `lib/domains/abused.txt` being updated in your PR
2. Automated review comments mentioning security/validation
3. Misunderstanding what the abused.txt file represents

**Your college is legitimate and was never tagged as fraud.**

## What Was Fixed

I have corrected the repository structure:
1. ✅ Removed `subodhpgcollege.txt` from root directory
2. ✅ Removed `file.zip` from root directory  
3. ✅ Created proper file at: `lib/domains/com/subodhpgcollege.txt`
4. ✅ Used the official name: "SS Jain Subodh PG College"

## How to Submit This Correctly to JetBrains

To submit this properly to the official JetBrains/swot repository:

1. **Fork JetBrains/swot** (if you haven't already)
2. **Create a new branch** from the latest master
3. **Add only one file**: `lib/domains/com/subodhpgcollege.txt` with content:
   ```
   SS Jain Subodh PG College
   ```
4. **Submit a PR** to JetBrains/swot with:
   - Title: "Add SS Jain Subodh PG College"
   - Description: Include college details, website URL, and proof that subodhpgcollege.com is the official domain

## Key Lessons

1. **File Placement Matters**: Always follow the repository's directory structure
2. **One Change Per PR**: Don't merge upstream changes when trying to add a single school
3. **Read Contributing Guidelines**: The CONTRIBUTING.md and README.md explain the exact process
4. **Domain Structure**: For domain `example.edu`, create file at `lib/domains/edu/example.txt`

## Resources

- JetBrains/swot repository: https://github.com/JetBrains/swot
- Contributing guidelines: https://github.com/JetBrains/swot/blob/master/CONTRIBUTING.md
- How to add a domain: See README.md section "How to add a domain to this repository"

## Conclusion

You did nothing wrong intentionally, and there was **no fraud accusation**. It was simply a technical mistake in file placement. The repository structure is specific, and it's easy to miss if you're new to contributing to this project.

Your college is legitimate, and with the proper file structure, your contribution should be accepted when submitted correctly to JetBrains/swot.
