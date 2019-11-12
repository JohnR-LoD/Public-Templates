<!-- Replace this line with one of the challenge formats below -->

<!--
Challenge Formats:
!INSTRUCTIONS[Azure Guided - Legacy Format](https://raw.githubusercontent.com/LODSContent/Public-Templates/master/Azure-Legacy/itpc-guided.md)
!INSTRUCTIONS[Azure Advanced - Legacy Format](https://raw.githubusercontent.com/LODSContent/Public-Templates/master/Azure-Legacy/itpc-advanced.md)
!INSTRUCTIONS[Azure Expert - Legacy Format](https://raw.githubusercontent.com/LODSContent/Public-Templates/master/Azure-Legacy/itpc-expert.md)
!INSTRUCTIONS[Guided](https://raw.githubusercontent.com/LODSContent/Public-Templates/master/Azure/itpc-guided.md)
!INSTRUCTIONS[Advanced](https://raw.githubusercontent.com/LODSContent/Public-Templates/master/Azure/itpc-advanced.md)
!INSTRUCTIONS[Expert](https://raw.githubusercontent.com/LODSContent/Public-Templates/master/Azure/itpc-expert.md)
-->

> [challenge-name]: Your Challenge Name!

> [overview]:
>
>

===
# Task heading

- Task step

- Task step

>#### Writing task steps in a guided challenge
The first step in any challenge should provide the instructions needed to sign in to the virtual machine or to the online services environment. After the first time you use Type Text or Copy to clipboard - generally the first step in a task - provide a tip on how to use the feature. 
- The sign in instruction style is a standard. Please use the language in this sample.
- The Type Text and Copy to clipboard tips are standard text. Please use the language in this sample.

##### Examples
- Sign in to @lab.VirtualMachine(YourLabVM).SelectLink as +++@lab.VirtualMachine(YourLabVM).Username+++ using +++@lab.VirtualMachine(YourLabVM).Password+++ as the password.

    >[!TIP] Select the +++Type Text+++ icon to enter the associated text into the virtual machine.

- Sign in to the Azure portal as ++@lab.CloudPortalCredential(LabAdmin).Username++ using ++@lab.CloudPortalCredential(LabAdmin).Password++ as the password.

    >[!TIP] Select the ++Copy to clipboard++ icon to copy the text string to the clipboard.

>In a guided challenge, each task will have at least one step that a user must perform in order to complete the task. In each instructional step, you tell the users what to do, provide any required input, and then if needed, finish the step by telling users what they should use to perform the action in the step. You want to tell them what to do, but not how to do it.
>If you switch virtual machines, or write an instruction that requires a user name or password, always provide the credentials. Don't make users go hunting for credentials.
>
##### Examples
-	Assign a Global admin role to Amy Rusko by using the Microsoft 365 admin center.
-	Configure Lori Penor’s mailbox to send an Out of Office message for both internal and external users.
-	Create a security group named Marketing Admins in the Corp | Groups organizational unit (OU).
-	Add two users named +++Darlene Rudd+++ and +++Sean Chai+++ to the **HR Admins** group.
>
>When you are writing tasks that require a user to use a specific cmdlet or method, provide the name of the cmdlet or method in the main instructional step, include a link to the documentation for that cmdlet or method if official documentation is available, and then put the complete code syntax in a hint.
>
>##### Example
-	Assign licenses to the new users by using the [Set-MsolUserLicense](“https://docs.microsoft.com/en-us/powershell/module/msonline/set-msoluserlicense?view=azureadps-1.0”) command.


>#### Use text boxes to store values
Use a text box to store a value that users will want to use later in the challenge — for example, an IP address, a URL, or a password. You can then retrieve the value by using an @lab variable. You can use this as copyable text in an instruction, or you can use it in a command.
- Text boxes and labels should be indented by four spaces.
- Press Tab after the label to force the text box onto a new line, without an extra line break.
- Test your text box by resizing the preview pane to ensure that the text box wraps to a new line.

##### Example

- Record the name of the data loss prevention (DLP) policy you created in the following text box:

    **DLP name**     
    @lab.TextBox(DLPRuleName)

    This is the value that you entered: @lab.Variable(DLPRuleName).


>#### Writing hints in a guided challenge
Use an expandable hint to provide users with the details of how to perform the action in the step. Hints can contain:
-	A video that steps users through what they need to do to perform the action in the step.
-	A screenshot that shows the correct configuration, and any UI elements the user must select in order to get to the configuration page.
-	An instructional step that uses the what / where / why structure.
-	The complete code syntax of any code that’s required.
>
>Each hint should describe one instructional step. Ideally, a user who knows the product in a challenge should be able to complete a task without any help. However, if a user is stuck on an individual step, you want to provide the user with the details of how to succeed. Users should be able to expand a hint for one step without seeing any other hints for the task. This allows users to challenge themselves to complete a task with little or no help.

##### Examples
- Assign licenses to the new users by using the [Set-MsolUserLicense](https://docs.microsoft.com/en-us/powershell/module/msonline/set-msoluserlicense?view=azureadps-1.0) command.

    >[!HINT]<details>
    ><summary>Expand this hint for guidance on assigning a license.</summary>
    >
    >- Run the following command to assign licenses by using Set-MsolUserLicense command:
    >
    >   ```
    >Get-MsolUser -UnlicensedUsersOnly | Set-MsolUserLicense -AddLicenses $sku
    >```
    >
    >   !IMAGE[SampleImage](Placeholder.jpg)
    >
    ></details>
 
- Remove the Office 365 E5 license assigned to Beth Burke by using the Microsoft 365 admin center.

    >[!HINT]<details>
    ><summary>Expand this hint for guidance on removing a license.</summary>
    >
    >- In the Microsoft 365 admin center, on the navigation menu, expand **Users**, and then select **Active users**.
    >
    >- Select **Beth Burke**, and then select **Manage product licenses**.
    >
    >   !IMAGE[SampleImage](Placeholder.jpg)
    >
    ></details>

## Check your work
- [] Confirm that you xxx.
- [] Confirm that you xxx.

>#### Writing Check your work statements
Each task must contain a check your work section after the task steps. 
-	Use one or more bulleted points that have check boxes.
-	Each point should begin with the word Confirm.
-	Each point should represent a key outcome of the task. It is possible that the points will not map directly to each step in the task, since you .
-	Do not put verification instructions in the check your work section. If users should perform a verification step, include this in the task steps.

##### Examples
- [] Confirm that you created user accounts for Frano Botica and Louisa Wall.
- [] Confirm that you assigned licenses to the new user accounts.
- [] Confirm that the Corp > Groups OU contains a security group named Network Admins.
- [] Confirm that you created a security group named Network Admins in the Corp > Groups OU.

===

# Summary

Congratulations, you have completed the **Your Challenge Title** challenge.

You have accomplished the following:

- Task one summary.
- Task two summary.

>#### Summary examples - please delete the samples
- Managed Active Directory group membership by using Group Policy.
- Enumerated Active Directory group membership by using Windows PowerShell.
- Created Office 365 user accounts.
- Created an Office 365 group.

##Your feedback is important!  
As you end your challenge, please take a few minutes to complete the short survey that will appear in the next window.

Alternatively, you may provide your feedback directly to <a href="mailto:challengefeedback@learnondemandsystems.com?Subject=LODS%20Challenge%20Feedback%20for%20Lab%20@lab.LabProfile.Id" target="_top">challengefeedback@learnondemandsystems.com</a>.

## Other IT Pro Challenges in this series

>This section is mandatory. Include any challenges in the series that relate to this challenge. Replace the sample titles, and delete this instruction paragraph. Leave one blank line between each challenge title.

- GUIDED CHALLENGE: xxxx

- ADVANCED CHALLENGE: Can You Create and Manage Active Directory Users and Groups?
