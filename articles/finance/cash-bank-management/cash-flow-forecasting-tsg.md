---
title: استكشاف أخطاء إعداد تقدير التدفقات النقدية وإصلاحها
description: يوفر هذا الموضوع أجوبة على الأسئلة التي قد تواجهك عند تكوين تقدير تدفق النقدية. ويتناول الأسئلة المتداولة حول إعداد التدفقات النقدية وتحديثات التدفق النقدي وPower BI للتدفق النقدي.
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 89eb2f1bcfc73a6a7171a275532b2356e858e87c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985277"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="c651a-104">استكشاف أخطاء إعداد تقدير التدفقات النقدية وإصلاحها</span><span class="sxs-lookup"><span data-stu-id="c651a-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c651a-105">يوفر هذا الموضوع أجوبة على الأسئلة التي قد تواجهك عند تكوين تقدير تدفق النقدية.</span><span class="sxs-lookup"><span data-stu-id="c651a-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="c651a-106">ويتناول الأسئلة المتداولة حول إعداد التدفقات النقدية وتحديثات التدفق النقدي وPower BI للتدفق النقدي.</span><span class="sxs-lookup"><span data-stu-id="c651a-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="c651a-107">لماذا يتم إظهار التدفق النقدي لكيان قانوني واحد فقط؟</span><span class="sxs-lookup"><span data-stu-id="c651a-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="c651a-108">يتم تكوين تقدير التدفقات النقدية وحسابها لكل كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="c651a-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="c651a-109">وتعرض تقارير Power BI وإمكانية تقديرات التدفقات النقدية في Finance insights النتائج.</span><span class="sxs-lookup"><span data-stu-id="c651a-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="c651a-110">يجب إعداد تقدير التدفقات النقدية لكل كيان قانوني ترغب في رؤية تنبؤ له.</span><span class="sxs-lookup"><span data-stu-id="c651a-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="c651a-111">راجع تكوين تقدير التدفق النقدي في كافة الكيانات القانونية.</span><span class="sxs-lookup"><span data-stu-id="c651a-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="c651a-112">بدلا من ذلك، قم بمراجعة تكوين كافة الكيانات القانونية لتقدير التدفقات النقدية، وتأكد من تعيينها كما كنت تقصد.</span><span class="sxs-lookup"><span data-stu-id="c651a-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="c651a-113">لماذا لا يُظهر  Power BI كافة بيانات التدفق النقدي؟</span><span class="sxs-lookup"><span data-stu-id="c651a-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="c651a-114">يجب إكمال العديد من الخطوات قبل أن تظهر تقديرات التدفقات النقدية في طرق عرض Power BI.</span><span class="sxs-lookup"><span data-stu-id="c651a-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="c651a-115">راجع قائمه الاختيار التالية، وتأكد من اكتمال كل خطوة:</span><span class="sxs-lookup"><span data-stu-id="c651a-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="c651a-116">قم بإعداد التدفق النقدي لكل كيان قانوني.</span><span class="sxs-lookup"><span data-stu-id="c651a-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="c651a-117">في معلمات دفتر الأستاذ العام، قم بتعيين عملة النظام ونوع سعر صرف للنظام.</span><span class="sxs-lookup"><span data-stu-id="c651a-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="c651a-118">قم بتعيين عملة محاسبة دفتر الأستاذ ونوع سعر الصرف.</span><span class="sxs-lookup"><span data-stu-id="c651a-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="c651a-119">أدخل أسعار الصرف بين عملة الحركة وعملة المحاسبة.</span><span class="sxs-lookup"><span data-stu-id="c651a-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="c651a-120">أدخل أسعار الصرف بين عملة المحاسبة وعملة الحركة.</span><span class="sxs-lookup"><span data-stu-id="c651a-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="c651a-121">أدخل أسعار الصرف بين عملة المحاسبة وكل عملة مصرفية.</span><span class="sxs-lookup"><span data-stu-id="c651a-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="c651a-122">لماذا يعمل Power BI للتدفق النقدي في الإصدارات السابقة ولكنه الآن فارغ؟</span><span class="sxs-lookup"><span data-stu-id="c651a-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="c651a-123">تحقق من تكوين قياسات "قياس التدفق النقدي V2" و "LedgerCovLiquidityMeasurement" من مخزن الكيانات.</span><span class="sxs-lookup"><span data-stu-id="c651a-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="c651a-124">لمزيد من المعلومات حول كيفية العمل مع البيانات في مخزن الكيانات، راجع [تكامل Power BI مع مخزن الكيانات](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) تحقق من اكتمال كافة الخطوات المطلوبة لعرض محتوى Power BI.</span><span class="sxs-lookup"><span data-stu-id="c651a-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="c651a-125">للحصول على مزيد من المعلومات، راجع [محتوى Power BI لنظرة عامة على النقدية](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="c651a-125">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="c651a-126">هل تم تحديث كيانات متجر الكيانات؟</span><span class="sxs-lookup"><span data-stu-id="c651a-126">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="c651a-127">يجب تحديث الكيانات بشكل دوري لضمان أن البيانات حديثة ودقيقة.</span><span class="sxs-lookup"><span data-stu-id="c651a-127">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="c651a-128">لتحديث كيان محدد يدويًا، انتقل إلى **إدارة النظام \> الإعداد \> متجر الكيانات**، وحدد الكيان، ثم حدد **تحديث**.</span><span class="sxs-lookup"><span data-stu-id="c651a-128">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="c651a-129">ويمكن أيضا تحديث البيانات تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="c651a-129">The data can also be updated automatically.</span></span> <span data-ttu-id="c651a-130">في صفحة **متجر البيانات**، قم بتعيين خيار **تمكين التحديث التلقائي** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="c651a-130">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>
