---
title: استكشاف أخطاء إعداد تقدير التدفقات النقدية وإصلاحها
description: يوفر هذا الموضوع أجوبة على الأسئلة التي قد تواجهك عند تكوين تقدير تدفق النقدية. ويتناول الأسئلة المتداولة حول إعداد التدفقات النقدية وتحديثات التدفق النقدي وPower BI للتدفق النقدي.
author: panolte
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b4760d7a0d0c14e2df8df20c2f81ec41e077cc0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827304"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="c0f99-104">استكشاف أخطاء إعداد تقدير التدفقات النقدية وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="c0f99-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0f99-105">يوفر هذا الموضوع أجوبة على الأسئلة التي قد تواجهك عند تكوين تقدير تدفق النقدية.</span><span class="sxs-lookup"><span data-stu-id="c0f99-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="c0f99-106">ويتناول الأسئلة المتداولة حول إعداد التدفقات النقدية وتحديثات التدفق النقدي وPower BI للتدفق النقدي.</span><span class="sxs-lookup"><span data-stu-id="c0f99-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="c0f99-107">لماذا يتم إظهار التدفق النقدي لكيان قانوني واحد فقط؟</span><span class="sxs-lookup"><span data-stu-id="c0f99-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="c0f99-108">يتم تكوين تقدير التدفقات النقدية وحسابها لكل كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="c0f99-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="c0f99-109">وتعرض تقارير Power BI وإمكانية تقديرات التدفقات النقدية في Finance insights النتائج.</span><span class="sxs-lookup"><span data-stu-id="c0f99-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="c0f99-110">يجب إعداد تقدير التدفقات النقدية لكل كيان قانوني ترغب في رؤية تنبؤ له.</span><span class="sxs-lookup"><span data-stu-id="c0f99-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="c0f99-111">راجع تكوين تقدير التدفق النقدي في كافة الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="c0f99-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="c0f99-112">بدلا من ذلك، قم بمراجعة تكوين كافة الكيانات القانونية لتقدير التدفقات النقدية، وتأكد من تعيينها كما كنت تقصد.</span><span class="sxs-lookup"><span data-stu-id="c0f99-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="c0f99-113">لماذا لا يُظهر  Power BI كافة بيانات التدفق النقدي؟</span><span class="sxs-lookup"><span data-stu-id="c0f99-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="c0f99-114">يجب إكمال العديد من الخطوات قبل أن تظهر تقديرات التدفقات النقدية في طرق عرض Power BI.</span><span class="sxs-lookup"><span data-stu-id="c0f99-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="c0f99-115">راجع قائمه الاختيار التالية، وتأكد من اكتمال كل خطوة:</span><span class="sxs-lookup"><span data-stu-id="c0f99-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="c0f99-116">قم بإعداد التدفق النقدي لكل كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="c0f99-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="c0f99-117">في معلمات دفتر الأستاذ العام، قم بتعيين عملة النظام ونوع سعر صرف للنظام.</span><span class="sxs-lookup"><span data-stu-id="c0f99-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="c0f99-118">قم بتعيين عملة محاسبة دفتر الأستاذ ونوع سعر الصرف.</span><span class="sxs-lookup"><span data-stu-id="c0f99-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="c0f99-119">أدخل أسعار الصرف بين عملة الحركة وعملة المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="c0f99-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="c0f99-120">أدخل أسعار الصرف بين عملة المحاسبة وعملة الحركة.</span><span class="sxs-lookup"><span data-stu-id="c0f99-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="c0f99-121">أدخل أسعار الصرف بين عملة المحاسبة وكل عملة مصرفية.</span><span class="sxs-lookup"><span data-stu-id="c0f99-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="c0f99-122">لماذا يعمل Power BI للتدفق النقدي في الإصدارات السابقة ولكنه الآن فارغ؟</span><span class="sxs-lookup"><span data-stu-id="c0f99-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="c0f99-123">تحقق من تكوين قياسات "قياس التدفق النقدي V2" و "LedgerCovLiquidityMeasurement" من مخزن الكيانات.</span><span class="sxs-lookup"><span data-stu-id="c0f99-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="c0f99-124">لمزيد من المعلومات حول كيفية التعامل مع البيانات في مخزن الكيانات، راجع [تكامل Power BI مع مخزن الكيانات](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="c0f99-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="c0f99-125">تحقق من اكتمال كل الخطوات المطلوبة لعرض محتوى Power BI.</span><span class="sxs-lookup"><span data-stu-id="c0f99-125">Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="c0f99-126">للحصول على مزيد من المعلومات، راجع [محتوى Power BI لنظرة عامة على النقدية](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="c0f99-126">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="c0f99-127">هل تم تحديث كيانات متجر الكيانات؟</span><span class="sxs-lookup"><span data-stu-id="c0f99-127">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="c0f99-128">يجب تحديث الكيانات بشكل دوري لضمان أن البيانات حديثة ودقيقة.</span><span class="sxs-lookup"><span data-stu-id="c0f99-128">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="c0f99-129">لتحديث كيان محدد يدويًا، انتقل إلى **إدارة النظام \> الإعداد \> متجر الكيانات**، وحدد الكيان، ثم حدد **تحديث**.</span><span class="sxs-lookup"><span data-stu-id="c0f99-129">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="c0f99-130">ويمكن أيضا تحديث البيانات تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="c0f99-130">The data can also be updated automatically.</span></span> <span data-ttu-id="c0f99-131">في صفحة **متجر البيانات**، قم بتعيين خيار **تمكين التحديث التلقائي** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="c0f99-131">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a><span data-ttu-id="c0f99-132">ما هي طريقة الحساب التي يجب استخدامها عند حساب تقديرات التدفقات النقدية؟</span><span class="sxs-lookup"><span data-stu-id="c0f99-132">Which calculation method should be used when calculating cash flow forecasts?</span></span>

<span data-ttu-id="c0f99-133">يحتوي أسلوب حساب تقدير التدفق النقدي علي خيارين هامين للتحديد.</span><span class="sxs-lookup"><span data-stu-id="c0f99-133">The Cash flow forecast calculation method has two important selection options.</span></span> <span data-ttu-id="c0f99-134">سيقوم الخيار **جديد** بحساب تقديرات التدفقات النقدية للمستندات والمستندات الجديدة التي تغيرت منذ تشغيل وظيفة المجموعة الاخيره.</span><span class="sxs-lookup"><span data-stu-id="c0f99-134">The **New** option will calculate cash flow forecasts for new documents and documents that have changed since the last batch job ran.</span></span> <span data-ttu-id="c0f99-135">يعمل هذا الخيار بشكل أسرع لأنه يعالج مجموعه فرعيه أصغر من المستندات.</span><span class="sxs-lookup"><span data-stu-id="c0f99-135">This option tends to run faster because it processes a smaller subset of documents.</span></span> <span data-ttu-id="c0f99-136">سيقوم الخيار **إجمالي** باعاده حساب تنبؤات التدفقات النقدية لكل مستند في النظام.</span><span class="sxs-lookup"><span data-stu-id="c0f99-136">The **Total** option will recalculate cash flow forecasts for every document in the system.</span></span> <span data-ttu-id="c0f99-137">يستغرق هذا الخيار وقتا إضافيا لإكمال المزيد من العمل.</span><span class="sxs-lookup"><span data-stu-id="c0f99-137">This option takes more time because it has more work to complete.</span></span>

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a><span data-ttu-id="c0f99-138">كيف يمكن تحسين أداء وظيفة مجموعه التكرارات المتكررة لتقدير التدفقات النقدية؟</span><span class="sxs-lookup"><span data-stu-id="c0f99-138">How do I improve the performance of the cash flow forecasting recurring batch job?</span></span>

<span data-ttu-id="c0f99-139">نوصي بتشغيل تقدير التدفقات النقدية مره واحده في كل يوم من الساعات القصوى باستخدام طريقه الحساب **الجديدة**.</span><span class="sxs-lookup"><span data-stu-id="c0f99-139">We recommend running your cash flow forecast once each day during the off-peak hours using the **New** calculation method.</span></span> <span data-ttu-id="c0f99-140">نوصي باستخدام هذه الطريقة لسته أيام لكل أسبوع.</span><span class="sxs-lookup"><span data-stu-id="c0f99-140">We recommend using this approach six days per week.</span></span> <span data-ttu-id="c0f99-141">قم بعد ذلك بتشغيل تقدير التدفقات النقدية مره واحده كل أسبوع باستخدام طريقة حساب **الإجمالي** في يوم بأقل قدر من النشاط.</span><span class="sxs-lookup"><span data-stu-id="c0f99-141">Then run a cash flow forecast once each week using the **Total** calculation method on the day with the least amount of activity.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

