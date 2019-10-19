---
title: إنشاء قواعد لمرشد تحسين الأداء
description: يناقش هذا الموضوع كيفية إضافة القواعد الجديدة إلى مرشد تحسين الأداء.
author: roxanadiaconu
manager: AnnBe
ms.date: 02/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: roxanad
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 27066cd860d78743d5ae7c851876eb62fe019245
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180980"
---
# <a name="create-rules-for-optimization-advisor"></a><span data-ttu-id="bcf76-103">إنشاء قواعد لمرشد تحسين الأداء</span><span class="sxs-lookup"><span data-stu-id="bcf76-103">Create rules for Optimization advisor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bcf76-104">يوضح هذا الموضوع كيفية إنشاء القواعد الجديدة لـ **مرشد تحسين الأداء**.</span><span class="sxs-lookup"><span data-stu-id="bcf76-104">This topic explains how to create new rules for **Optimization advisor**.</span></span> <span data-ttu-id="bcf76-105">على سبيل المثال، يمكنك إنشاء قاعدة جديدة لتحديد حالات طلبات عروض الأسعار‬ (RFQ) التي تشتمل على عنوان فارغ.</span><span class="sxs-lookup"><span data-stu-id="bcf76-105">For example, you can create a new rule that identifies which Request for Quotations (RFQ) cases have an empty title.</span></span> <span data-ttu-id="bcf76-106">استخدام العناوين في الحالات يجعل من السهل تحديدها والبحث عنها.</span><span class="sxs-lookup"><span data-stu-id="bcf76-106">Using titles on cases makes them easily identifiable and searchable.</span></span> <span data-ttu-id="bcf76-107">بينما هذا المثال بسيط جدًا، يوضح ما يمكن تحقيقه باستخدام قواعد تحسين الأداء.</span><span class="sxs-lookup"><span data-stu-id="bcf76-107">While quite simple, this example shows what can be achieved with optimization rules.</span></span> 

<span data-ttu-id="bcf76-108">*القاعدة* هي علامة اختيار في بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="bcf76-108">A *rule* is a check on application data.</span></span> <span data-ttu-id="bcf76-109">إذا تم الوفاء بالشرط الذي تقيمه القاعدة، يتم إنشاء فرص لتحسين العمليات أو البيانات.</span><span class="sxs-lookup"><span data-stu-id="bcf76-109">If the condition that the rule evaluates is met, opportunities to optimize processes or improve data are created.</span></span> <span data-ttu-id="bcf76-110">يمكن تنفيذ الفرص ويمكن قياس تأثير الإجراءات بشكل اختياري.</span><span class="sxs-lookup"><span data-stu-id="bcf76-110">The opportunities can be acted upon and, optionally, the impact of the actions can be measured.</span></span> 

<span data-ttu-id="bcf76-111">لإنشاء قاعدة جديدة لـ **مرشد التحسين**، أضف فئة جديدة توسع الفئة المجردة **SelfHealingRule** وتنفذ واجهة **IDiagnosticsRule** ويتم تزيينها بالسمة **DiagnosticRule**.</span><span class="sxs-lookup"><span data-stu-id="bcf76-111">To create a new rule for the **Optimization advisor**, add a new class that extends the **SelfHealingRule** abstract class, implements the **IDiagnosticsRule** interface, and is decorated by the **DiagnosticRule** attribute.</span></span> <span data-ttu-id="bcf76-112">كما يجب أن تشتمل الفئة على أسلوب مزين بالسمة **DiagnosticsRuleSubscription**.</span><span class="sxs-lookup"><span data-stu-id="bcf76-112">The class must also have a method decorated with the **DiagnosticsRuleSubscription** attribute.</span></span> <span data-ttu-id="bcf76-113">بشكل تقليدي، يتم إجراء هذا في أسلوب **opportunityTitle** الذي ستتم مناقشته لاحقًا.</span><span class="sxs-lookup"><span data-stu-id="bcf76-113">By convention, that is done on the **opportunityTitle** method, which will be discussed later.</span></span> <span data-ttu-id="bcf76-114">يمكن إضافة هذه الفئة الجديدة إلى نموذج مخصص باستخدام تبعية في نموذج **SelfHealingRules**.</span><span class="sxs-lookup"><span data-stu-id="bcf76-114">This new class can be added to a custom model with a dependency on the **SelfHealingRules** model.</span></span> <span data-ttu-id="bcf76-115">في المثال التالي، تُسمى القاعدة الجاري تنفيذها **RFQTitleSelfHealingRule**.</span><span class="sxs-lookup"><span data-stu-id="bcf76-115">In the following example, the rule being implemented is called **RFQTitleSelfHealingRule**.</span></span>

```
[DiagnosticsRule] 
public final class RFQTitleSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule 
{ 
… 
} 
```

<span data-ttu-id="bcf76-116">تشتمل الفئة المجردة **SelfHealingRule** على أساليب مجردة يجب تنفيذها في الفئات القديمة.</span><span class="sxs-lookup"><span data-stu-id="bcf76-116">The **SelfHealingRule** abstract class has abstract methods that must be implemented in inheriting classes.</span></span> <span data-ttu-id="bcf76-117">الذاكرة الأساسية هي أسلوب **التقييم** الأسلوب الذي يقوم بإرجاع قائمة بالفرص المحددة بواسطة القاعدة.</span><span class="sxs-lookup"><span data-stu-id="bcf76-117">The core is the **evaluate** method, which returns a list of the opportunities identified by the rule.</span></span> <span data-ttu-id="bcf76-118">يمكن أن تكون الفرص حسب الكيان القانوني أو يمكن تطبيقها على النظام بالكامل.</span><span class="sxs-lookup"><span data-stu-id="bcf76-118">Opportunities can be per legal entity or can apply to the whole system.</span></span>

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

<span data-ttu-id="bcf76-119">يدور الأسلوب الموضح أعلاه عبر الشركات ويحدد حالات RFQ بالعناوين الفارغة في أسلوب **findRFQCasesWithEmptyTitle**.</span><span class="sxs-lookup"><span data-stu-id="bcf76-119">The method shown above loops over companies and selects RFQ cases with empty titles in the **findRFQCasesWithEmptyTitle** method.</span></span> <span data-ttu-id="bcf76-120">إذا تم العثور على حالة واحدة على الأقل، فإنه يتم إنشاء فرصة خاصة بالشركة باستخدام أسلوب **getOpportunityForCompany**.</span><span class="sxs-lookup"><span data-stu-id="bcf76-120">If at least one such case is found, then a company-specific opportunity is created with the **getOpportunityForCompany** method.</span></span> <span data-ttu-id="bcf76-121">لاحظ أن الحقل **بيانات** في جدول **SelfHealingOpportunity** من نوع **الحاوية**، ولذلك يمكنه أن يحتوي على أي بيانات تتعلق بالمنطق الخاص بهذه القاعدة.</span><span class="sxs-lookup"><span data-stu-id="bcf76-121">Notice that the field **Data** in the **SelfHealingOpportunity** table is of type **Container**, and can therefore contain any data relevant to the logic specific to this rule.</span></span> <span data-ttu-id="bcf76-122">يسجل الإعداد **OpportunityDate** مع الطابع الزمني الحالي وقت آخر تقييم للفرصة.</span><span class="sxs-lookup"><span data-stu-id="bcf76-122">Setting **OpportunityDate** with the current timestamp registers the time of the latest evaluation of the opportunity.</span></span>  

<span data-ttu-id="bcf76-123">يمكن أن تكون الفرص عبر الشركة.</span><span class="sxs-lookup"><span data-stu-id="bcf76-123">Opportunities can also be cross-company.</span></span> <span data-ttu-id="bcf76-124">في هذه الحالة، تكون شركات الدوران غير ضرورية ويجب إنشاء الفرصة باستخدام أسلوب **getOpportunityAcrossCompanies**.</span><span class="sxs-lookup"><span data-stu-id="bcf76-124">In this case, the loop over companies is not necessary and the opportunity must be created with the **getOpportunityAcrossCompanies** method.</span></span> 

<span data-ttu-id="bcf76-125">يعرض الرمز التالي أسلوب **findRFQCasesWithEmptyTitle**، الذي يعرض معرفات حالات طلب عروض الأسعار التي تشتمل على عناوين فارغة.</span><span class="sxs-lookup"><span data-stu-id="bcf76-125">The following code shows the **findRFQCasesWithEmptyTitle** method, which returns the IDs of the RFQ cases that have empty titles.</span></span>

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

<span data-ttu-id="bcf76-126">كما أن هناك أسلوبان يجب استخدامهما هما **opportunityTitle** و**opportunityDetails**.</span><span class="sxs-lookup"><span data-stu-id="bcf76-126">Two more methods that must be implemented are **opportunityTitle** and **opportunityDetails**.</span></span> <span data-ttu-id="bcf76-127">الأول يعرض عنوانًا قصيرًا للفرصة، بينما الأخر يعرض وصفًا تفصيليًا للفرصة، التي قد تشتمل على بيانات.</span><span class="sxs-lookup"><span data-stu-id="bcf76-127">The former returns a short title for the opportunity, the latter returns a detailed description of the opportunity, which can also include data.</span></span>

<span data-ttu-id="bcf76-128">يظهر العنوان المعروض بواسطة **opportunityTitle** تحت عمود **فرصة التحسين** في مساحة عمل **مرشد التحسين**.</span><span class="sxs-lookup"><span data-stu-id="bcf76-128">The title returned by **opportunityTitle** appears under the **Optimization opportunity** column in the **Optimization advisor** workspace.</span></span> <span data-ttu-id="bcf76-129">كما يظهر كعنوان للجزء الجانبي ويعرض مزيدًا من المعلومات حول الفرصة.</span><span class="sxs-lookup"><span data-stu-id="bcf76-129">It also appears as the header of the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="bcf76-130">بشكل تقليدي، يتم تزيين هذا الأسلوب باستخدام السمة **DiagnosticRuleSubscription** التي تأخذ الوسائط التالية:</span><span class="sxs-lookup"><span data-stu-id="bcf76-130">By convention, this method is decorated with the **DiagnosticRuleSubscription** attribute, which takes the following arguments:</span></span> 

* <span data-ttu-id="bcf76-131">**منطقة التشخيص** – تعداد من النوع **DiagnosticArea** يصف مساحة التطبيق التي تنتمي إليها القاعدة، مثل **DiagnosticArea::SCM**.</span><span class="sxs-lookup"><span data-stu-id="bcf76-131">**Diagnostic area** – An enum of type **DiagnosticArea** that describes what area of the application the rule belongs to, such as **DiagnosticArea::SCM**.</span></span> 

* <span data-ttu-id="bcf76-132">**اسم القاعدة** -سلسلة تحتوي على اسم القاعدة.</span><span class="sxs-lookup"><span data-stu-id="bcf76-132">**Rule name** – A string with the rule name.</span></span> <span data-ttu-id="bcf76-133">سيظهر هذا الاسم ضمن عمود **اسم القاعدة** في نموذج **قاعدة التحقق من صحة التشخيصات** (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="bcf76-133">This will appear under the **Rule name** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

* <span data-ttu-id="bcf76-134">**معدل تكرار التشغيل‬** – تعداد من النوع **DiagnosticRunFrequency** يصف عدد مرات تشغيل القاعدة المطلوب، مثل **DiagnosticRunFrequency::Daily**.</span><span class="sxs-lookup"><span data-stu-id="bcf76-134">**Run frequency** – An enum of type **DiagnosticRunFrequency** that describes how often the rule should be run, such as **DiagnosticRunFrequency::Daily**.</span></span> 

* <span data-ttu-id="bcf76-135">**وصف القاعدة** - سلسلة تحتوي على وصف أكثر تفصيلاً للقاعدة.</span><span class="sxs-lookup"><span data-stu-id="bcf76-135">**Rule description** – A string with a more detailed description of the rule.</span></span> <span data-ttu-id="bcf76-136">سيظهر هذا ضمن عمود **وصف القاعدة** في نموذج **قاعدة التحقق من صحة التشخيصات** (**DiagnosticsValidationRuleMaintain**).</span><span class="sxs-lookup"><span data-stu-id="bcf76-136">This will appear under the **Rule description** column in the **Dianostics validation rule** form (**DiagnosticsValidationRuleMaintain**).</span></span> 

> [!NOTE]
> <span data-ttu-id="bcf76-137">السمة **DiagnosticRuleSubscription** مطلوبة لكي تعمل القاعدة.</span><span class="sxs-lookup"><span data-stu-id="bcf76-137">The **DiagnosticRuleSubscription** attribute is required for the rule to work.</span></span> <span data-ttu-id="bcf76-138">وعادةً ما يتم استخدامها في **opportunityTitle**، ولكن يمكنها تزيين أي أسلوب للفئة.</span><span class="sxs-lookup"><span data-stu-id="bcf76-138">Typically, it is used on **opportunityTitle**, but it can decorate any method of the class.</span></span>

<span data-ttu-id="bcf76-139">التالي هو مثال للتنفيذ.</span><span class="sxs-lookup"><span data-stu-id="bcf76-139">The following is an example implementation.</span></span> <span data-ttu-id="bcf76-140">يتم استخدام السلاسل الأولية لتحقيق البساطة، ولكن يتطلب التنفيذ الصحيح وجود ملصقات.</span><span class="sxs-lookup"><span data-stu-id="bcf76-140">Raw strings are used for simplicity, but a correct implementation requires labels.</span></span> 

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

<span data-ttu-id="bcf76-141">يظهر الوصف المعروض بواسطة **opportunityDetails** على الجزء الجانبي ويعرض مزيدًا من المعلومات حول الفرصة.</span><span class="sxs-lookup"><span data-stu-id="bcf76-141">The description returned by **opportunityDetails** appears on the side pane showing more information about the opportunity.</span></span> <span data-ttu-id="bcf76-142">يأخذ هذا الوسيطة **SelfHealingOpportunity** التي هي عبارة عن حقل **بيانات** يمكن استخدامه لتوفير المزيد من التفاصيل حول الفرصة.</span><span class="sxs-lookup"><span data-stu-id="bcf76-142">This takes the **SelfHealingOpportunity** argument, which is **Data** field that can be used to provide more details about the opportunity.</span></span> <span data-ttu-id="bcf76-143">في المثال، يعرض الأسلوب معرفات حالات RFQ المشتملة على عنوان فارغ.</span><span class="sxs-lookup"><span data-stu-id="bcf76-143">In the example, the method returns the IDs of the RFQ cases with an empty title.</span></span> 

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

<span data-ttu-id="bcf76-144">الأسلوبان المجردان المتبقيان للتنفيد هما **provideHealingAction** و**securityMenuItem**.</span><span class="sxs-lookup"><span data-stu-id="bcf76-144">The two remaining abstract methods to implement are **provideHealingAction** and **securityMenuItem**.</span></span> 

<span data-ttu-id="bcf76-145">يعرض **provideHealingAction** "حقيق" إذا تم توفير إجراء علاج، وإلا، فإنه يعرض "زائف".</span><span class="sxs-lookup"><span data-stu-id="bcf76-145">**provideHealingAction** returns true if a healing action is provided, otherwise, it returns false.</span></span> <span data-ttu-id="bcf76-146">في حالة عرض "حقيقي"، يجب تنفيذ الأسلوب **performAction** وإلا سيظهر خطأ.</span><span class="sxs-lookup"><span data-stu-id="bcf76-146">If true is returned, the method **performAction** must be implemented, or an error will be thrown.</span></span> <span data-ttu-id="bcf76-147">أسلوب **performAction** يأخذ وسيطة **SelfHealingOpportunity**، التي يمكن فيها استخدام البيانات للإجراء.</span><span class="sxs-lookup"><span data-stu-id="bcf76-147">The **performAction** method takes a **SelfHealingOpportunity** argument, in which the data can be used for the action.</span></span> <span data-ttu-id="bcf76-148">في المثال، يفتح الإجراء **PurchRFQCaseTableListPage** للتصحيح اليدوي.</span><span class="sxs-lookup"><span data-stu-id="bcf76-148">In the example, the action opens the **PurchRFQCaseTableListPage**, for manual correction.</span></span> 

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

<span data-ttu-id="bcf76-149">استنادًا إلى مواصفات القاعدة، قد يكون من الممكن اتخاذ إجراء تلقائي باستخدام بيانات الفرصة.</span><span class="sxs-lookup"><span data-stu-id="bcf76-149">Depending on the specifics of the rule, it might be possible to take an automatic action using the opportunity data.</span></span> <span data-ttu-id="bcf76-150">في هذا المثال، قد يستطيع النظام إنشاء عناوين لحالات RFQ تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="bcf76-150">In this example, the system could generate titles for RFQ cases automatically.</span></span> 

<span data-ttu-id="bcf76-151">يعرض **securityMenuItem** اسم عنصر قائمة إجراءات لأن القاعدة تكون مرئية فقط للمستخدمين الذين يمكنهم الوصول إلى عنصر قائمة الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="bcf76-151">**securityMenuItem** returns the name of an action menu item such that the rule is only visible to users who can access the action menu item.</span></span> <span data-ttu-id="bcf76-152">قد يتطلب الأمان إمكانية وصول المستخدمين المصرح لهم فقط إلى الفرص والقواعد الخاصة.</span><span class="sxs-lookup"><span data-stu-id="bcf76-152">Security might require that specific rules and opportunities are accessible only to authorized users.</span></span> <span data-ttu-id="bcf76-153">في المثال، يستطيع فقط المستخدمون الذين لديهم وصول إلى **PurchRFQCaseTitleAction** عرض الفرصة.</span><span class="sxs-lookup"><span data-stu-id="bcf76-153">In the example, only users with access to **PurchRFQCaseTitleAction** can view the opportunity.</span></span> <span data-ttu-id="bcf76-154">لاحظ أن عنصر قائمة الإجراءات هذا تم إنشاؤه لهذا المثال، وتمت إضافته كنقطة إدخال لامتياز أمان **PurchRFQCaseTableMaintain**.</span><span class="sxs-lookup"><span data-stu-id="bcf76-154">Notice that this action menu item was created for this example, and was added as an entry point for the **PurchRFQCaseTableMaintain** security privilege.</span></span> 

> [!NOTE]
> <span data-ttu-id="bcf76-155">يجب أن يكون عنصر القائمة عبارة عن عنصر قائمة إجراءات لكي يعمل الأمان بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="bcf76-155">The menu item must be an action menu item for security to work correctly.</span></span> <span data-ttu-id="bcf76-156">لن تعمل أنواع عناصر القائمة الأخرى، مثل **عرض عناصر القائمة** بشكل صحيح.</span><span class="sxs-lookup"><span data-stu-id="bcf76-156">Other menu item types, such as **Display menu items** will not work correctly.</span></span>

```
public MenuName securityMenuItem() 
{ 
    return menuItemActionStr(PurchRFQCaseTitleAction); 
}
```

<span data-ttu-id="bcf76-157">بعد تأليف القاعدة، قم بتنفيذ الوظيفة التالية لعرضها في واجهة المستخدم (UI).</span><span class="sxs-lookup"><span data-stu-id="bcf76-157">After the rule has compiled, execute the following job to have it display in the user interface (UI).</span></span>

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

<span data-ttu-id="bcf76-158">ستظهر القاعدة في نموذج **قاعدة التحقق من صحة التشخيصات**، وهي متوفرة من **إدارة النظام** > **المهام الدورية** > **صيانة قاعدة التحقق من صحة التشخيصات**.</span><span class="sxs-lookup"><span data-stu-id="bcf76-158">The rule will display in the **Diagnostics validation rule** form, available from **System administration** > **Periodic tasks** > **Maintain diagnostics validation rule**.</span></span> <span data-ttu-id="bcf76-159">ولتقييمها، انتقل إلى **إدارة النظام** > **المهام الدورية** > **قاعدة التحقق من صحة تشخيصات الجدول‬**، وحدد عدد مرات تكرار القاعدة، مثل **يوميًا**.</span><span class="sxs-lookup"><span data-stu-id="bcf76-159">To have it evaluated, go to **System administration** > **Periodic tasks** > **Schedule diagnostics validation rule**, select the frequency of the rule, such as **Daily**.</span></span> <span data-ttu-id="bcf76-160">وانقر فوق **موافق**.</span><span class="sxs-lookup"><span data-stu-id="bcf76-160">Click **OK**.</span></span> <span data-ttu-id="bcf76-161">انتقل إلى **إدارة النظام** > **مرشد التحسين** لعرض الفرصة الجديدة.</span><span class="sxs-lookup"><span data-stu-id="bcf76-161">Go to **System administration** > **Optimization advisor** to view the new opportunity.</span></span> 

<span data-ttu-id="bcf76-162">المثال التالي عبارة عن أجزاء من تعليمات برمجية مع إطار عمل قاعدة تتضمن كافة الأساليب والسمات المطلوبة.</span><span class="sxs-lookup"><span data-stu-id="bcf76-162">The following example is a code snippet with the skeleton of a rule including all the required methods and attributes.</span></span> <span data-ttu-id="bcf76-163">من شأنه أن يساعدك في بدء كتابة قواعد جديدة.</span><span class="sxs-lookup"><span data-stu-id="bcf76-163">It helps you get started with writing new rules.</span></span><span data-ttu-id="bcf76-164"> التسميات وعناصر قائمة الإجراءات المستخدمة في المثال هي مستخدمة فقط لأغراض العرض التوضيحي.</span><span class="sxs-lookup"><span data-stu-id="bcf76-164"> The labels and action menu items that are used in the example are only used for demonstration purpose.</span></span>

```
[DiagnosticsRuleAttribute]
public final class SkeletonSelfHealingRule extends SelfHealingRule implements IDiagnosticsRule
{
    [DiagnosticsRuleSubscription(DiagnosticsArea::SCM,
                                 "@SkeletonRuleLabels:SkeletonRuleTitle", // Label with the title of the rule
                                 DiagnosticsRunFrequency::Monthly,
                                 "@SkeletonRuleLabels:SkeletonRuleDescription")] // Label with a description of the rule
    public str opportunityTitle()
    {
        // Return a label with the title of the opportunity
        return "@SkeletonRuleLabels:SkeletonOpportunityTitle";
    }

    public str opportunityDetails(SelfHealingOpportunity _opportunity)
    {
        str details = "";

        // Use _opportunity.data to provide details on the opportunity

        return details;
    }

    protected List evaluate()
    {
        List results = new List(Types::Record);

        // Write here the core logic of the rule

        // When creating an opportunity, use:
        //     * this.getOpportunityForCompany() for company specific opportunities
        //     * this.getOpportunityAcrossCompanies() for cross-company opportunities

        return results;
    }

    public boolean providesHealingAction()
    {
        return true;
    }

    protected void performAction(SelfHealingOpportunity _opportunity)
    {
        // Place here the code that performs the healing action

        // To open a form, use the following:
        // new MenuFunction(menuItemDisplayStr(SkeletonRuleDisplayMenuItem), MenuItemType::Display).run();
    }

    public MenuName securityMenuItem()
    {
        return menuItemActionStr(SkeletonRuleActionMenuItem);
    }

}
```

<span data-ttu-id="bcf76-165">لمزيد من المعلومات، شاهد مقطع الفيديو القصير على YouTube: [مرشد التحسين في Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span><span class="sxs-lookup"><span data-stu-id="bcf76-165">For more information, watch the short YouTube video: [Optimization advisor in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ)</span></span>
