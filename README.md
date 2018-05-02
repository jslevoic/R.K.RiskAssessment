# R.K.RiskAssessment



The RK Risk Assessment is an interpretation of other industry accepted Risk Assessment Guidence. The "Asset and Attack Vector" methodology. Some may even view this as simply a method of organizing an Asset Focused risk assessment.


PURPOSE
There are two main purposes for why this RK Risk Assessment is being posted:
  - Current Risk Assessment guidence found online is lacking in the implementation guidence and/or real world example. A lot
    of language is put into the description of 'various phases', but allow for a very large variance in interpetation. This 
    may be by design to allow for broader adoption. That being said it seems to be too broad in some cases, leaving 
    organization confused and often implementing somewhat useless risk assessments to check a box. **The Purpose** of this
    Risk Assessment Methodology is to hopfully provide more concrete and/or useable guidence.
    
  - It is being posted to hear any feedback, thoughts, or criticism that can potentially allow for improvement to the RK 
    Risk Assessment Methodology/Interpretation. 
  
  
IMPORTANT NOTES
  - There may be this exact methodology/guidence somewhere else on the internet. Only a few minutes were spent trying to 
    find 
    the exact same thing. If it already exists, I apologize for wasting your time.
  - Before implementing this methodology, make sure to research other Risk Assessment Guidence such as NIST 800-30, 
    ISO27005, OCTAVE, etc.. This will allow you to make more informed decisions as to which approach works best for you. 
  - This approach is Not For Everyone and may not work for your organization or network layout!!  
    

DEFINITIONS
It is important to acknowledge the definitions utilized in this explaination. Various cyber security definitions vary dependiong on the speak/organization writing it. Just because something is defined within this Guide in a certain manner, does not mean that definition is the only definition or way to interpret a word. These definitions are provided to ensure clarity in reading this Guide. 

  - Threat Actor / Threat Source : this is the human or non-human entity that is carrying out the threat. This entity 
    utilizes a vulnerability (or attack vector) to cause the impact. 
    
  - Threat Event / Threat : this is the event that occurs that is caused by the threat actor. Typically this is the whole
    statement "A malicious outsider compromising a system via phishing attack"
    
  - Likelihood : The probability (chance) that the above threat event occurs. 
  
  - Impact : The consequence of the above threat event taking place. Can include financial impact, reputational impact, etc.
  
  - Risk : The Likelihood x The Impact 
  
  - Inherent ___ : The initial ___ that is measured. For example, inherent likelihood is the likelihood of the threat event
    taking place without any controls in place. For the purpose of the RK Risk Assessment, the inherent likelihood, inherent
    inherent impact, and inherent risk takes into account only what is Public-Facing vs Non-Public-Facing, that 
    systems/application requires an 8 character password. It **does** take the assumption that there is no internal network 
    segmentation, no role based access control, etc.  
          -- Why does it take these assumption?   Because it allows you to document segmentation as a control, it allows you
             to document role based access control as a control. If you were to ignore the basic Public-Facing vs 
             Non-Public-Facing, then this "Attack Vector Based Approach" wouldnt be possible.
          -- These assumptions can be changed based on how it affects your network and your organization. 
             
             
OVERVIEW
It should be fairly common knowledge that there are different ways to perform a risk assessment. Some risk assessments focus on starting with identifying as many threat sources and threat actors that you can, then moving on to their motivation, what they may be after, etc. Some risk assessments focus on starting with the enumeration of assets, and identifying all threats to that asset. 

The RK Risk Asessment puts an emphasis on Attack Vector first and foremost. It is mainly focused on non-accidental threats, but can potentially be modified to include accidental and compliance threats. It is advised that you perform multiple different risk and threat assessments based on your context. For instance, when thinking about risks posed by threats to your internally developed application, you would want a more indepth analysis covering everything from session handling to user input, and then roll that into the over all risk of your "Company Application" within this risk assessment. 

But back to the overview. 

Again the RK Risk Assessment focuses on the path in which an adversary can cause an impact, which makes this a fairly easy to understand methodology.


METHODOLOGY (example pictures to come)
  1.  Make your table headers. Across the top row starting with the first column, write:
      Asset | Secondary Asset | Threat Event | Inherent Likelihood | Inherent Impact | Inherent Risk | Description of Impact 
                  | Inherent Risk | Controls | What Might The Controls Miss | Residual Likelihood | Residual Impact | 
                        | Residual Risk | Potential Controls | Future Plans 
                        
                             ----The above should all be in the same row.
  
  2.  List out all of the technology that you have in the left most column of an Excel Spread Sheet. During this first round 
      through you can focus on things that are somewhat important. Although there is a threat to every piece of technology 
      or process you have, going through 150+ may be a daunting first task. Once a first important round is completed, feel 
      free to go back and add the next 20+ applications or assets. Feel free to follow the example pictures. Organize it so 
      that all of the systems/devices that Regularly Take Direct User Input at the top of the Excel Sheet, just to allow you 
      to focus on them first. For instance, typically you should place "HR Employee Laptop" at the top, followed by maybe 
      "Engineer/Dev Employee Laptop", maybe a "publically accessable web app", "VPN Soultion" or SaaS solution etc. (you 
      know, things that can allow access to other things... kinda shows the attack vector focus). But you really dont have 
      to worry about the order, all of your assets should be listed at somepoint down the first collumn.
      
      
      
   3. Now, start going though those Direct User Input Assets. Write out all of the threats you can think of to them. Ask
      people around you, think outside the box. 
   
   4. Once the excel sheet is "Filled In" (besides that "Secondary Asset Column") its time to fill that "secondary Asset
      Column" in. Any other assets that are 1 direct attack vector away should be listed under each. This may take a handful
      of copy/paste to fill them all in. (hopefully in the future there will be an application that automatically links
      things so you dont have to fill in the same thing multiple time.) 
      
      **You should not yet be filling in the threat events, likelihoods, impacts etc. for the secondary assets, only what 
      the secondary assets are**
      
      For example, once a hand full of threats are written beside "HR Laptop" (there should be multiple rows with the asset       "HR Laptop", one row for each threat) then you will determine "okay, now taking the stance that the HR Laptop is 
      compromised, what else can I reach".
      
      There will be multiple new rows inserted of the new threats posed by that first asset being compromised.
      
      
      
   5. Now that the threats to the assets -which are one attack vector away- are enumerated, fill in the likelihood with the
      same residual likelihood of the originally compromised asset (unless there is a specific reason why not to). This is
      because if the original laptop is compromised, and you are looking at the INITIAL likelihood without any controls in 
      place, you should be able to assume that the secondary asset is compromised.
      
      
   6. Fill in everything else as you would.
   
   
   7. Rinse and repeat. Add more specific assets. Remember to include physical threats (tornado, fire, etc.) to every asset 
      in the first column that you see fit. 
      
      
 

    
  
  
  
  
  
  
  
  
  
