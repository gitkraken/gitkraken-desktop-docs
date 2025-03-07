---

title: Conflict Prevention in Gitkraken
description: Learn about conflict prevention in Gitkraken Desktop
taxonomy:
    category: gitkraken-desktop

---
# **Conflict Prevention in GitKraken**  

Merge conflicts can be a major pain, whether they happen during your coding session or while reviewing work. They often lead to delays, rework, and frustration.  

GitKraken Desktop’s **Conflict Prevention** helps you detect and manage potential conflicts before they cause disruptions.  

<img src="/wp-content/uploads/GKD-conflict-prevention.png" class="help-center-img img-bordered">

---

## **Conflict Prevention**  

GitKraken detects potential merge conflicts with **Org Members** based on overlapping edits in committed changes that haven’t yet been merged into your target branch.  

### **How It Works:**  

#### **1. Conflict Alert Icon**  
After a coding session, open GitKraken Desktop If potential conflicts exist, you’ll see an **alert icon**.

<img src="/wp-content/uploads/GKD-org-member-conflict.png" class="help-center-img img-bordered">

#### **2. Click the Alert Icon**  

This will open a conflict detection menu with options to manage conflicts.  

<img src="/wp-content/uploads/GKD-unfurl-org-member-conflict.png" class="help-center-img img-bordered">

<div class='callout callout--success'>
    <p>The active conflict with the target takes priority over org member potential conflicts. The potential conflicts only show up if you don't have an active conflict with the target, not the other way around.</p>
</div>

#### **3. Resolve Conflicts Proactively**  
- Share edits as a **Cloud Patch**.  
- Push your changes (if they aren’t already pushed).  
- Copy a summary of overlapping edits to share with team members.  

## **Target Branch Status**
### **What if You Don't Have Org Members?**  
- Even without Org Members, GitKraken will still proactively detect conflicts between your branch and its target branch so you can resolve them before they get worse.  
- You’ll be able to **rebase or merge** to resolve conflicts. 

<img src="/wp-content/uploads/GKD-non-org-conflict-menu.png" class="help-center-img img-bordered">

### **When No Conflicts Are Detected**
If there are no conflicts detected with your target branch and there are no overlapping edits with other org members’ branches, you will see a target branch status indicator to confirm there are no conflicts with the target branch. The menu provides a quick open to open a pull request against the target branch or adjust your target branch preferences for the repository.

<img src="/wp-content/uploads/GKD-no-conflict-detected-with-PR.png" class="help-center-img img-bordered">

### **Want to Detect Conflicts Even Earlier?**  

You can invite the **author of the conflicting changes** directly from the conflict detection menu. 

<img src="/wp-content/uploads/GKD-invite-org-member-conflict.png" class="help-center-img img-bordered">

Once they’re in your GitKraken organization, you’ll be notified as soon as they are editing in the same areas as you - no need to wait for the changes to merge into the target branch.