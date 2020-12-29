---
title: استخدم البيانات الخارجية في تقديرات التدفق النقدي (معاينة)
description: يصف هذا الموضوع خطوات الإعداد التي يجب إكمالها بحيث يمكن إدخال البيانات الخارجية أو استيرادها إلى تقديرات التدفقات النقدية.
author: rcarlson
manager: AnnBe
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 801327dc54f6d4cfef7a9f062395e29846783e8f
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644935"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="16c0c-103">استخدم البيانات الخارجية في تقديرات التدفق النقدي (معاينة)</span><span class="sxs-lookup"><span data-stu-id="16c0c-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="16c0c-104">يمكن إدخال البيانات الخارجية أو استيرادها إلى تقديرات تدفقات نقدية.</span><span class="sxs-lookup"><span data-stu-id="16c0c-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="16c0c-105">يصف هذا الموضوع خطوات الإعداد الخاصة باستخدام البيانات الخارجية والتي تمكن من تضمين البيانات الخارجية في تقدير التدفقات النقدية.</span><span class="sxs-lookup"><span data-stu-id="16c0c-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="16c0c-106">إعداد البيانات الخارجية</span><span class="sxs-lookup"><span data-stu-id="16c0c-106">External data setup</span></span>

<span data-ttu-id="16c0c-107">استخدم علامة التبويب **المصدر الخارجي** في الصفحة **إعداد تقدير التدفقات النقدية** (**إدارة النقد والبنوك \> تقدير التدفقات النقدية‬**) لإدخال الإعدادات التي تدعم استخدام البيانات الخارجية في تقديرات التدفقات النقدية.</span><span class="sxs-lookup"><span data-stu-id="16c0c-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="16c0c-108">للحصول على المزيد من المعلومات حول الإعداد، راجع [تقدير التدفقات النقدية](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span><span class="sxs-lookup"><span data-stu-id="16c0c-108">For more information about the setup, see [Cash flow forecasting](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span></span>

<span data-ttu-id="16c0c-109">لإدخال بيانات خارجية لتقديرات التدفقات النقدية، يمكنك استخدام خبرات فتح في Excel‬ لإدخال البيانات الخارجية وتعديلها.</span><span class="sxs-lookup"><span data-stu-id="16c0c-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="16c0c-110">حدد الزر **البيانات الخارجية**، ثم حدد إما **إضافة بيانات خارجية** أو **تحرير البيانات الخارجية الموجودة**.</span><span class="sxs-lookup"><span data-stu-id="16c0c-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="16c0c-111">عند فتح الملف Microsoft Excel، فإنه يمكنك إدخال معلومات في الحقول التالية:</span><span class="sxs-lookup"><span data-stu-id="16c0c-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="16c0c-112">**معرف الإدخال**</span><span class="sxs-lookup"><span data-stu-id="16c0c-112">**Entry ID**</span></span>
- <span data-ttu-id="16c0c-113">**الوصف** (اختياري)</span><span class="sxs-lookup"><span data-stu-id="16c0c-113">**Description** (optional)</span></span>
- <span data-ttu-id="16c0c-114">**اسم المصدر الخارجي** – حدد إحدى القيم في القائمة التي قمت بتحديدها عند إعداد Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="16c0c-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="16c0c-115">**كيان قانوني**</span><span class="sxs-lookup"><span data-stu-id="16c0c-115">**Legal Entity**</span></span>
- <span data-ttu-id="16c0c-116">**التاريخ**</span><span class="sxs-lookup"><span data-stu-id="16c0c-116">**Date**</span></span>
- <span data-ttu-id="16c0c-117">**المبلغ بعملة الحركة**</span><span class="sxs-lookup"><span data-stu-id="16c0c-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="16c0c-118">**كود العملة**</span><span class="sxs-lookup"><span data-stu-id="16c0c-118">**Currency Code**</span></span>
- <span data-ttu-id="16c0c-119">**البعد الافتراضي** (اختياري)</span><span class="sxs-lookup"><span data-stu-id="16c0c-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="16c0c-120">**رقم المستند** (اختياري)</span><span class="sxs-lookup"><span data-stu-id="16c0c-120">**Document number** (optional)</span></span>
- <span data-ttu-id="16c0c-121">**رقم الحساب** (اختياري)</span><span class="sxs-lookup"><span data-stu-id="16c0c-121">**Account number** (optional)</span></span>
- <span data-ttu-id="16c0c-122">**اسم الحساب** (اختياري)</span><span class="sxs-lookup"><span data-stu-id="16c0c-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="16c0c-123">استيراد بيانات خارجية باستخدام إطار عمل إدارة البيانات</span><span class="sxs-lookup"><span data-stu-id="16c0c-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="16c0c-124">يمكنك استيراد البيانات الخارجية لتقديرات التدفقات النقدية باستخدام مساحة عمل **إدارة البيانات** والكيان المسمى **إدخال مصدر خارجي لتقدير التدفقات النقدية**.</span><span class="sxs-lookup"><span data-stu-id="16c0c-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="16c0c-125">بالإضافة إلى ذلك، إذا كان من الضروري نقل بيانات الإعداد من بيئة إلى أخرى، تصبح منطقة الكيانات التالية متاحة لجداول الإعداد المطلوبة:</span><span class="sxs-lookup"><span data-stu-id="16c0c-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="16c0c-126">إعداد المصدر الخارجي للتنبؤ بالتدفق النقدي</span><span class="sxs-lookup"><span data-stu-id="16c0c-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="16c0c-127">إعداد الكيان القانوني للمصدر الخارجي للتنبؤ بالتدفق النقدي</span><span class="sxs-lookup"><span data-stu-id="16c0c-127">Cash flow forecast external source legal entity setup</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="16c0c-128">إشعار الخصوصية</span><span class="sxs-lookup"><span data-stu-id="16c0c-128">Privacy notice</span></span>
<span data-ttu-id="16c0c-129">إن المعاينات (1) قد تستخدم تدابير أقل تتعلق بالخصوصية وإجراءات الأمان مقارنةً بخدمة Dynamics 365 Finance and Operations‏، و(2) لا يتم تضمينها في اتفاقية مستوى الخدمة (SLA) لهذه الخدمة، و(3) يجب ألا يتم استخدامها لمعالجة البيانات الشخصية أو البيانات الأخرى التي تخضع لمتطلبات التوافق القانونية أو التنظيمية، و(4) هي ذات دعم محدود.</span><span class="sxs-lookup"><span data-stu-id="16c0c-129">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
