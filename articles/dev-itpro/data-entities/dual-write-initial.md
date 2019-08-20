---
title: أمر التنفيذ للمزامنة الأولية بين Finance and Operations وCommon Data Service
description: يحدد هذا الموضوع ترتيب المزامنة التي يجب اتباعها لإنشاء البيانات الأولية.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797288"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="c98d5-103">أمر التنفيذ للمزامنة الأولية بين Finance and Operations وCommon Data Service</span><span class="sxs-lookup"><span data-stu-id="c98d5-103">Execution order for initial sychronization of Finance and Operations and Common Data Service</span></span>

<span data-ttu-id="c98d5-104">قبل استخدام تكامل البيانات، يجب إنشاء البيانات الأولية المطلوبة للعملاء والموردين وجهات الاتصال.</span><span class="sxs-lookup"><span data-stu-id="c98d5-104">Before you use data integration, you must create the initial data required for customers, vendors and contacts.</span></span> <span data-ttu-id="c98d5-105">على سبيل المثال، إذا أردت إنشاء صنف **مجموعة موردين** وتعيين **شروط الدفع** على شكل **Net30**، فقبل أن تحاول إنشاء صنف **مجموعة الموردين** يجب أن تتأكد من وجود **Net30** في كل من Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="c98d5-105">For example, if you want to create a new **Vendor group** item and set its **Terms of Payment** as **Net30**, then before you attempt to create the **Vendor group** item you need to make sure that **Net30** exists in both Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="c98d5-106">(في المستقبل، سنقوم بإصدار وظيفة نظام أساسي للكتابة المزدوجة تسمى **المزامنة الأولية**. ستجري هذه الوظيفة مزامنة بيانات لمرة واحدة بين Finance and Operations وCommon Data Service كجزء من إعداد الكتابة المزدوجة.)</span><span class="sxs-lookup"><span data-stu-id="c98d5-106">(In the future, we will release a  dual-write platform functionality called **Initial Sync**. It will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

<span data-ttu-id="c98d5-107">نصائح: نحن بصدد إصار خريطة كتابة مزدوجة لجميع البيانات المرجعية بما في ذلك **شروط الدفع** (شروط الدفع).</span><span class="sxs-lookup"><span data-stu-id="c98d5-107">Tips: We are releasing a dual-write map for all reference data including **Terms of Payment** (Payment Terms).</span></span> <span data-ttu-id="c98d5-108">إذا كانت البيانات الأولية موجودة في نظام واحد، فبإمكان عملية تحديث صغيرة على سجل أن تؤدي تشغيل الكتابة المزدوجة على هذا السجل.</span><span class="sxs-lookup"><span data-stu-id="c98d5-108">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span> 

<span data-ttu-id="c98d5-109">يجب اتباع ترتيب الأسبقية التالي والتأكد من توفر البيانات الأولية في كل من Finance and Operations وCommon Data Service.</span><span class="sxs-lookup"><span data-stu-id="c98d5-109">You must follow the following order of precedence and make sure that the initial data is available on both Finance and Operations and Common Data Service.</span></span>   

## <a name="vendor"></a><span data-ttu-id="c98d5-110">المورد</span><span class="sxs-lookup"><span data-stu-id="c98d5-110">Vendor</span></span>

<span data-ttu-id="c98d5-111">ترتيب التنفيذ للمورّد هو:</span><span class="sxs-lookup"><span data-stu-id="c98d5-111">The order of execution for Vendor is:</span></span>

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a><span data-ttu-id="c98d5-112">العميل (مؤسسة)</span><span class="sxs-lookup"><span data-stu-id="c98d5-112">Customer (Organization)</span></span>

<span data-ttu-id="c98d5-113">ترتيب التنفيذ للعميل هو:</span><span class="sxs-lookup"><span data-stu-id="c98d5-113">The order of execution for Customer is:</span></span>

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a><span data-ttu-id="c98d5-114">جهة الاتصال (شخص)</span><span class="sxs-lookup"><span data-stu-id="c98d5-114">Contact (Person)</span></span>

<span data-ttu-id="c98d5-115">ترتيب التنفيذ لجهة الاتصال هو:</span><span class="sxs-lookup"><span data-stu-id="c98d5-115">The order of execution for Contact is:</span></span>

```
Customer
Vendor               
```
