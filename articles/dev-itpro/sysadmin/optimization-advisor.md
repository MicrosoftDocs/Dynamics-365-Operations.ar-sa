---
title: "إنشاء قواعد لمرشد تحسين الأداء"
description: "يناقش هذا الموضوع كيفية إضافة القواعد الجديدة إلى مرشد تحسين الأداء."
author: roxanadiaconu
manager: AnnBe
ms.date: 01/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core (Operations, Core)
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 9cb9343028acacc387370e1cdd2202b84919185e
ms.openlocfilehash: 88739298405343a36ae5bc11f51c666c414e7157
ms.contentlocale: ar-sa
ms.lasthandoff: 01/23/2018

---

# <a name="create-rules-for-optimization-advisor"></a><span data-ttu-id="d4791-103">إنشاء قواعد لمرشد تحسين الأداء</span><span class="sxs-lookup"><span data-stu-id="d4791-103">Create rules for Optimization advisor</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d4791-104">يوضح هذا الموضوع كيفية إنشاء القواعد الجديدة لـ **مرشد تحسين الأداء**.</span><span class="sxs-lookup"><span data-stu-id="d4791-104">This topic explains how to create new rules for **Optimization advisor**.</span></span> <span data-ttu-id="d4791-105">على سبيل المثال، يمكنك إنشاء قاعدة جديدة لتحديد حالات طلبات عروض الأسعار‬ (RFQ) التي تشتمل على عنوان فارغ.</span><span class="sxs-lookup"><span data-stu-id="d4791-105">For example, you can create a new rule that identifies which Request for Quotations (RFQ) cases have an empty title.</span></span> <span data-ttu-id="d4791-106">استخدام العناوين في الحالات يجعل من السهل تحديدها والبحث عنها.</span><span class="sxs-lookup"><span data-stu-id="d4791-106">Using titles on cases makes them easily identifiable and searchable.</span></span> <span data-ttu-id="d4791-107">بينما هذا المثال بسيط جدًا، يوضح ما يمكن تحقيقه باستخدام قواعد تحسين الأداء.</span><span class="sxs-lookup"><span data-stu-id="d4791-107">While quite simple, this example shows what can be achieved with optimization rules.</span></span> 

<span data-ttu-id="d4791-108">*القاعدة* هي علامة اختيار في بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="d4791-108">A *rule* is a check on application data.</span></span> <span data-ttu-id="d4791-109">إذا تم الوفاء بالشرط الذي تقيمه القاعدة، يتم إنشاء فرص لتحسين العمليات أو البيانات.</span><span class="sxs-lookup"><span data-stu-id="d4791-109">If the condition that the rule evaluates is met, opportunities to optimize processes or improve data are created.</span></span> <span data-ttu-id="d4791-110">يمكن تنفيذ الفرص ويمكن قياس تأثير الإجراءات بشكل اختياري.</span><span class="sxs-lookup"><span data-stu-id="d4791-110">The opportunities can be acted upon and, optionally, the impact of the actions can be measured.</span></span> 

<span data-ttu-id="d4791-111">لإنشاء قاعدة جديدة لـ **مرشد التحسين**، أضف فئة جديدة توسع الفئة المجردة **SelfHealingRule** وتنفذ واجهة **IDiagnosticsRule** ويتم تزيينها بالسمة **DiagnosticRule**.</span><span class="sxs-lookup"><span data-stu-id="d4791-111">To create a new rule for the **Optimization advisor**, add a new class that extends the **SelfHealingRule** abstract class, implements the **IDiagnosticsRule** interface, and is decorated by the **DiagnosticRule** attribute.</span></span> <span data-ttu-id="d4791-112">كما يجب أن تشتمل الفئة على أسلوب مزين بالسمة **DiagnosticsRuleSubscription**.</span><span class="sxs-lookup"><span data-stu-id="d4791-112">The class must also have a method decorated with the **DiagnosticsRuleSubscription** attribute.</span></span> <span data-ttu-id="d4791-113">بشكل تقليدي، يتم إجراء هذا في أسلوب **opportunityTitle** الذي ستتم مناقشته لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="d4791-113">By convention, that is done on the **opportunityTitle** method, which will be discussed later.</span></span> <span data-ttu-id="d4791-114">يمكن إضافة هذه الفئة الجديدة إلى نموذج مخصص باستخدام تبعية في نموذج **SelfHealingRules**.</span><span class="sxs-lookup"><span data-stu-id="d4791-114">This new class can be added to a custom model with a dependency on the **SelfHealingRules** model.</span></span> <span data-ttu-id="d4791-115">في المثال التالي، تُسمى القاعدة الجاري تنفيذها **RFQTitleSelfHealingRule**.</span><span class="sxs-lookup"><span data-stu-id="d4791-115">In the following example, the rule being implemented is called **RFQTitleSelfHealingRule**.</span></span>

```
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

<span data-ttu-id="d4791-116">تشتمل الفئة المجردة **SelfHealingRule** على أساليب مجردة يجب تنفيذها في الفئات القديمة.</span><span class="sxs-lookup"><span data-stu-id="d4791-116">The **SelfHealingRule** abstract class has abstract methods that must be implemented in inheriting classes.</span></span> <span data-ttu-id="d4791-117">الذاكرة الأساسية هي أسلوب **التقييم** الأسلوب الذي يقوم بإرجاع قائمة بالفرص المحددة بواسطة القاعدة.</span><span class="sxs-lookup"><span data-stu-id="d4791-117">The core is the **evaluate** method, which returns a list of the opportunities identified by the rule.</span></span> <span data-ttu-id="d4791-118">يمكن أن تكون الفرص حسب الكيان القانوني أو يمكن تطبيقها على النظام بالكامل.</span><span class="sxs-lookup"><span data-stu-id="d4791-118">Opportunities can be per legal entity or can apply to the whole system.</span></span>

```
protected List evaluate() 
{ 
    List results = new List(Types::Record); 
    
    DataArea dataArea; 

    while select id from dataArea 
        where !dataArea.isVirtual 
    { 
        changecompany(dataArea.id) 
        { 
            container result = this.findRFQCasesWithEmptyTitle(); 

            if (conLen(result) > 0) 
            { 
                SelfHealingOpportunity opportunity = this.getOpportunityForCompany(dataArea.Id); 
                opportunity.EvaluationState = SelfHealingEvaluationState::Evaluated; 
                opportunity.Data = result; 
                opportunity.OpportunityDate = DateTimeUtil::utcNow(); 
                
                results.addEnd(opportunity); 
            } 
        } 
    } 
    
    return results; 
} 
```

<span data-ttu-id="d4791-119">يدور الأسلوب الموضح أعلاه عبر الشركات ويحدد حالات RFQ بالعناوين الفارغة في أسلوب **findRFQCasesWithEmptyTitle**.</span><span class="sxs-lookup"><span data-stu-id="d4791-119">The method shown above loops over companies and selects RFQ cases with empty titles in the **findRFQCasesWithEmptyTitle** method.</span></span> <span data-ttu-id="d4791-120">إذا تم العثور على حالة واحدة على الأقل، فإنه يتم إنشاء فرصة خاصة بالشركة باستخدام أسلوب **getOpportunityForCompany**.</span><span class="sxs-lookup"><span data-stu-id="d4791-120">If at least one such case is found, then a company-specific opportunity is created with the **getOpportunityForCompany** method.</span></span> <span data-ttu-id="d4791-121">لاحظ أن الحقل **بيانات** في جدول **SelfHealingOpportunity** من نوع **الحاوية**، ولذلك يمكنه أن يحتوي على أي بيانات تتعلق بالمنطق الخاص بهذه القاعدة.</span><span class="sxs-lookup"><span data-stu-id="d4791-121">Notice that the field **Data** in the **SelfHealingOpportunity** table is of type **Container**, and can therefore contain any data relevant to the logic specific to this rule.</span></span> <span data-ttu-id="d4791-122">يسجل الإعداد **OpportunityDate** مع الطابع الزمني الحالي وقت آخر تقييم للفرصة.</span><span class="sxs-lookup"><span data-stu-id="d4791-122">Setting **OpportunityDate** with the current timestamp registers the time of the latest evaluation of the opportunity.</span></span>  

<span data-ttu-id="d4791-123">يمكن أن تكون الفرص عبر الشركة.</span><span class="sxs-lookup"><span data-stu-id="d4791-123">Opportunities can also be cross-company.</span></span> <span data-ttu-id="d4791-124">في هذه الحالة، تكون شركات الدوران غير ضرورية ويجب إنشاء الفرصة باستخدام أسلوب **getOpportunityAcrossCompanies**.</span><span class="sxs-lookup"><span data-stu-id="d4791-124">In this case, the loop over companies is not necessary and the opportunity must be created with the **getOpportunityAcrossCompanies** method.</span></span> 

<span data-ttu-id="d4791-125">يعرض الرمز التالي أسلوب **findRFQCasesWithEmptyTitle**، الذي يعرض معرفات حالات طلب عروض الأسعار التي تشتمل على عناوين فارغة.</span><span class="sxs-lookup"><span data-stu-id="d4791-125">The following code shows the **findRFQCasesWithEmptyTitle** method, which returns the IDs of the RFQ cases that have empty titles.</span></span>

```
private container findRFQCasesWithEmptyTitle() 
{ 
    container result; 

    PurchRFQCaseTable rfqCase; 
    while select RFQCaseId from rfqCase 
        where rfqCase.Name == '' 
    { 
        result += rfqCase.RFQCaseId; 
    } 
    
    return result; 
} 
```

<span data-ttu-id="d4791-126">كما أن هناك أسلوبان يجب استخدامهما هما **opportunityTitle** و**opportunityDetails**.</span><span class="sxs-lookup"><span data-stu-id="d4791-126">Two more methods that must be implemented are **opportunityTitle** and **opportunityDetails**.</span></span> <span data-ttu-id="d4791-127">الأول يعرض عنوانًا قصيرًا للفرصة، بينما الأخر يعرض وصفًا تفصيليًا للفرصة، التي قد تشتمل على بيانات.</span><span class="sxs-lookup"><span data-stu-id="d4791-127">The former returns a short title for the opportunity, the latter returns a detailed description of the opportunity, which can also include data.</span></span>

<span data-ttu-id="d4791-128">يظهر العنوان المعروض بواسطة **opportunityTitle** تحت عمود **فرصة التحسين** في مساحة عمل **مرشد التحسين**.</span><span class="sxs-lookup"><span data-stu-id="d4791-128">The title returned by **opportunityTitle** appears under the **Optimization opportunity** column in the **Optimization advisor** workspace.</span></span> <span data-ttu-id="d4791-129">كما يظهر كعنوان للجزء الجانبي ويعرض مزيدًا من المعلومات حول الفرصة.</span><span class="sxs-lookup"><span data-stu-id="d4791-129">It also appears as the header of the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="d4791-130">بشكل تقليدي، يتم تزيين هذا الأسلوب باستخدام السمة **DiagnosticRuleSubscription** التي تأخذ الوسائط التالية:</span><span class="sxs-lookup"><span data-stu-id="d4791-130">By convention, this method is decorated with the **DiagnosticRuleSubscription** attribute, which takes the following arguments:</span></span> 

* <span data-ttu-id="d4791-131">**منطقة التشخيص** - تعداد نوع **DiagnosticArea** الذي يصف مساحة التطبيق التي تنتمي إليها القاعدة، مثل **DiagnosticArea::SCM**.</span><span class="sxs-lookup"><span data-stu-id="d4791-131">**Diagnostic area** – An enum of type **DiagnosticArea** that describes what area of the application the rule belongs to, such as **DiagnosticArea::SCM**.</span></span> 

* <span data-ttu-id="d4791-132">**اسم القاعدة** -سلسلة تحتوي على اسم القاعدة.</span><span class="sxs-lookup"><span data-stu-id="d4791-132">**Rule name** – A string with the rule name.</span></span> <span data-ttu-id="d4791-133">سيظهر هذا الاسم ضمن عمود **اسم القاعدة** في نموذج **قاعدة التحقق من صحة التشخيصات** (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="d4791-133">This will appear under the **Rule name** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

* <span data-ttu-id="d4791-134">**تشغيل معدل التكرار** - تعداد من نوع **DiagnosticRunFrequency** يوضح عدد مرات التي يجب بها تشغيل القاعدة، مثل **DiagnosticRunFrequency::Daily**.</span><span class="sxs-lookup"><span data-stu-id="d4791-134">**Run frequency** – An enum of type **DiagnosticRunFrequency** that describes how often the rule should be run, such as **DiagnosticRunFrequency::Daily**.</span></span> 

* <span data-ttu-id="d4791-135">**وصف القاعدة** - سلسلة تحتوي على وصف أكثر تفصيلاً للقاعدة.</span><span class="sxs-lookup"><span data-stu-id="d4791-135">**Rule description** – A string with a more detailed description of the rule.</span></span> <span data-ttu-id="d4791-136">سيظهر هذا ضمن عمود **وصف القاعدة** في نموذج **قاعدة التحقق من صحة التشخيصات** (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="d4791-136">This will appear under the **Rule description** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

> [!NOTE]
> <span data-ttu-id="d4791-137">السمة **DiagnosticRuleSubscription** مطلوبة لكي تعمل القاعدة.</span><span class="sxs-lookup"><span data-stu-id="d4791-137">The **DiagnosticRuleSubscription** attribute is required for the rule to work.</span></span> <span data-ttu-id="d4791-138">وعادةً ما يتم استخدامها في **opportunityTitle**، ولكن يمكنها تزيين أي أسلوب للفئة.</span><span class="sxs-lookup"><span data-stu-id="d4791-138">Typically, it is used on **opportunityTitle**, but it can decorate any method of the class.</span></span>

<span data-ttu-id="d4791-139">التالي هو مثال للتنفيذ.</span><span class="sxs-lookup"><span data-stu-id="d4791-139">The following is an example implementation.</span></span> <span data-ttu-id="d4791-140">يتم استخدام السلاسل الأولية لتحقيق البساطة، ولكن يتطلب التنفيذ الصحيح وجود ملصقات.</span><span class="sxs-lookup"><span data-stu-id="d4791-140">Raw strings are used for simplicity, but a correct implementation requires labels.</span></span> 

```
[DiagnosticsRuleSubscription(DiagnosticsArea::SCM, 
                             'Assign titles to Request for Quotation cases', 
                             DiagnosticsRunFrequency::Daily,  
                             'This rule detects Requests for Quotation with empty titles.')] 
public str opportunityTitle() 
{ 
    return 'Assign titles to Request for Quotation cases'; 
} 
```

<span data-ttu-id="d4791-141">يظهر الوصف المعروض بواسطة **opportunityDetails** على الجزء الجانبي ويعرض مزيدًا من المعلومات حول الفرصة.</span><span class="sxs-lookup"><span data-stu-id="d4791-141">The description returned by **opportunityDetails** appears on the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="d4791-142">يأخذ هذا الوسيطة **SelfHealingOpportunity** التي هي عبارة عن حقل **بيانات** يمكن استخدامه لتوفير المزيد من التفاصيل حول الفرصة.</span><span class="sxs-lookup"><span data-stu-id="d4791-142">This takes the **SelfHealingOpportunity** argument, which is **Data** field that can be used to provide more details about the opportunity.</span></span> <span data-ttu-id="d4791-143">في المثال، يعرض الأسلوب معرفات حالات RFQ المشتملة على عنوان فارغ.</span><span class="sxs-lookup"><span data-stu-id="d4791-143">In the example, the method returns the IDs of the RFQ cases with an empty title.</span></span> 

```
public str opportunityDetails(SelfHealingOpportunity _opportunity) 
{ 
    str details = ''; 
    container opportunityData = _opportunity.Data; 
    int affectedRFQCasesCount = conLen(opportunityData); 

    if (affectedRFQCasesCount != 0) 
    { 
        details = 'The following Request for Quotation cases have an empty title:\n'; 
        for (int i = 1; i <= affectedRFQCasesCount ; i++) 
        { 
            PurchRFQCaseId rfqCaseId = conPeek(opportunityData, i); 
            details += rfqCaseId + '\n'; 
        } 
    } 

    return details; 
}
```

<span data-ttu-id="d4791-144">الأسلوبان المجردان المتبقيان للتنفيد هما **provideHealingAction** و**securityMenuItem**.</span><span class="sxs-lookup"><span data-stu-id="d4791-144">The two remaining abstract methods to implement are **provideHealingAction** and **securityMenuItem**.</span></span> 

<span data-ttu-id="d4791-145">يعرض **provideHealingAction** "حقيق" إذا تم توفير إجراء علاج، وإلا، فإنه يعرض "زائف".</span><span class="sxs-lookup"><span data-stu-id="d4791-145">**provideHealingAction** returns true if a healing action is provided, otherwise, it returns false.</span></span> <span data-ttu-id="d4791-146">في حالة عرض "حقيقي"، يجب تنفيذ الأسلوب **performAction** وإلا سيظهر خطأ.</span><span class="sxs-lookup"><span data-stu-id="d4791-146">If true is returned, the method **performAction** must be implemented, or an error will be thrown.</span></span> <span data-ttu-id="d4791-147">أسلوب **performAction** يأخذ وسيطة **SelfHealingOpportunity**، التي يمكن فيها استخدام البيانات للإجراء.</span><span class="sxs-lookup"><span data-stu-id="d4791-147">The **performAction** method takes a **SelfHealingOpportunity** argument, in which the data can be used for the action.</span></span> <span data-ttu-id="d4791-148">في المثال، يفتح الإجراء **PurchRFQCaseTableListPage** للتصحيح اليدوي.</span><span class="sxs-lookup"><span data-stu-id="d4791-148">In the example, the action opens the **PurchRFQCaseTableListPage**, for manual correction.</span></span> 

```
public boolean providesHealingAction() 
{ 
    return true; 
} 

protected void performAction(SelfHealingOpportunity _opportunity) 
{ 
    new MenuFunction(menuItemDisplayStr(PurchRFQCaseTableListPage), MenuItemType::Display).run(); 
} 
```

<span data-ttu-id="d4791-149">استنادًا إلى مواصفات القاعدة، قد يكون من الممكن اتخاذ إجراء تلقائي باستخدام بيانات الفرصة.</span><span class="sxs-lookup"><span data-stu-id="d4791-149">Depending on the specifics of the rule, it might be possible to take an automatic action using the opportunity data.</span></span> <span data-ttu-id="d4791-150">في هذا المثال، قد يستطيع النظام إنشاء عناوين لحالات RFQ تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="d4791-150">In this example, the system could generate titles for RFQ cases automatically.</span></span> 

<span data-ttu-id="d4791-151">يعرض **securityMenuItem** اسم عنصر قائمة إجراءات لأن القاعدة تكون مرئية فقط للمستخدمين الذين يمكنهم الوصول إلى عنصر قائمة الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="d4791-151">**securityMenuItem** returns the name of an action menu item such that the rule is only visible to users who can access the action menu item.</span></span> <span data-ttu-id="d4791-152">قد يتطلب الأمان إمكانية وصول المستخدمين المصرح لهم فقط إلى الفرص والقواعد الخاصة.</span><span class="sxs-lookup"><span data-stu-id="d4791-152">Security might require that specific rules and opportunities are accessible only to authorized users.</span></span> <span data-ttu-id="d4791-153">في المثال، يستطيع فقط المستخدمون الذين لديهم وصول إلى **PurchRFQCaseTitleAction** عرض الفرصة.</span><span class="sxs-lookup"><span data-stu-id="d4791-153">In the example, only users with access to **PurchRFQCaseTitleAction** can view the opportunity.</span></span> <span data-ttu-id="d4791-154">لاحظ أن عنصر قائمة الإجراءات هذا تم إنشاؤه لهذا المثال، وتمت إضافته كنقطة إدخال لامتياز أمان **PurchRFQCaseTableMaintain**.</span><span class="sxs-lookup"><span data-stu-id="d4791-154">Notice that this action menu item was created for this example, and was added as an entry point for the **PurchRFQCaseTableMaintain** security privilege.</span></span> 

```
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

<span data-ttu-id="d4791-155">بعد تأليف القاعدة، قم بتنفيذ الوظيفة التالية لعرضها في واجهة المستخدم (UI).</span><span class="sxs-lookup"><span data-stu-id="d4791-155">After the rule has compiled, execute the following job to have it display in the user interface (UI).</span></span>

```
class ScanNewRulesJob 
{         
    public static void main(Args _args) 
    {         
        SysExtensionCache::clearAllScopes(); 
        var controller = new DiagnosticsRuleController(); 
        controller.runOperation(); 
    } 
} 
```

<span data-ttu-id="d4791-156">ستظهر القاعدة في نموذج **قاعدة التحقق من صحة التشخيصات**، وهي متوفرة من **إدارة النظام** > **المهام الدورية** > **صيانة قاعدة التحقق من صحة التشخيصات**.</span><span class="sxs-lookup"><span data-stu-id="d4791-156">The rule will display in the **Diagnostics validation rule** form, available from **System administration** > **Periodic tasks** > **Maintain diagnostics validation rule**.</span></span> <span data-ttu-id="d4791-157">ولتقييمها، انتقل إلى **إدارة النظام** > **المهام الدورية** > **قاعدة التحقق من صحة تشخيصات الجدول‬**، وحدد عدد مرات تكرار القاعدة، مثل **يوميًا**.</span><span class="sxs-lookup"><span data-stu-id="d4791-157">To have it evaluated, go to **System administration** > **Periodic tasks** > **Schedule diagnostics validation rule**, select the frequency of the rule, such as **Daily**.</span></span> <span data-ttu-id="d4791-158">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="d4791-158">Click **OK**.</span></span> <span data-ttu-id="d4791-159">انتقل إلى **إدارة النظام** > **مرشد التحسين** لعرض الفرصة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="d4791-159">Go to **System administration** > **Optimization advisor** to view the new opportunity.</span></span> 

<span data-ttu-id="d4791-160">لمزيد من المعلومات، شاهد هذا الفيديو القصير على YouTube:</span><span class="sxs-lookup"><span data-stu-id="d4791-160">For more information, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/MRsAzgFCUSQ]

