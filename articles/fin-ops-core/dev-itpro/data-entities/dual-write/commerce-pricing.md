---
title: استخدام محرك التسعير لـ Dynamics 365 Commerce مع Dynamics 365 Sales
description: يصف هذا الموضوع كيفية استخدام محرك التسعير في Microsoft Dynamics 365 Commerce لإنشاء عروض أسعار المبيعات في Dynamics 365 Sales.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: fad5c21d75db62b85efe803f1667dd3f9164a5fc
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594908"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a><span data-ttu-id="f0475-103">استخدام محرك التسعير لـ Dynamics 365 Commerce مع Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="f0475-103">Use the Dynamics 365 Commerce pricing engine with Dynamics 365 Sales</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f0475-104">يصف هذا الموضوع كيفية استخدام محرك التسعير في Microsoft Dynamics 365 Commerce لإنشاء عروض أسعار المبيعات في Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="f0475-104">This topic describes how to use the Microsoft Dynamics 365 Commerce pricing engine to create sales quotations in Dynamics 365 Sales.</span></span>

<span data-ttu-id="f0475-105">يدعم محرك التسعير في Dynamics 365 Commerce معظم سيناريوهات التسعير من الشركات إلى المستهلك (B2C)، مثل التسعير على مستوى المتجر، والتسعير المستند إلى الانتماء والقائم على الولاء، وخصومات المزيج والمطابقة، وخصومات الكمية، وخصومات الحد الأدنى.</span><span class="sxs-lookup"><span data-stu-id="f0475-105">The Dynamics 365 Commerce pricing engine supports most business-to-consumer (B2C) pricing scenarios, such as store-level pricing, affiliation-based and loyalty-based pricing, mix-and-match discounts, quantity discounts, and threshold discounts.</span></span> <span data-ttu-id="f0475-106">يستخدم محرك التسعير قواعد معقدة لتحديد أفضل سعر لعرض أسعار أو أمر معين.</span><span class="sxs-lookup"><span data-stu-id="f0475-106">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span>

<span data-ttu-id="f0475-107">عند استخدام [الكتابة الثنائية](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview)، تتوفر لديك ثلاثه خيارات لاحتياجات التسعير الخاصة بك.</span><span class="sxs-lookup"><span data-stu-id="f0475-107">When you use [dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), you have three options for your pricing needs.</span></span> <span data-ttu-id="f0475-108">يمكنك استخدام التسعير الثابت الذي يأتي من قائمة الأسعار في Dynamics 365 Sales أو محرك التسعير في Dynamics 365 Supply Chain Management أو محرك التسعير في Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f0475-108">You can use the static pricing that comes from the price list in Dynamics 365 Sales, the pricing engine in Dynamics 365 Supply Chain Management, or the pricing engine in Dynamics 365 Commerce.</span></span> <span data-ttu-id="f0475-109">من بين هذه الخيارات، يعد محرك التسعير التجاري الأنسب لسيناريوهات العمل إلى المستهلك.</span><span class="sxs-lookup"><span data-stu-id="f0475-109">Among these options, the Commerce pricing engine is best suited to B2C scenarios.</span></span>

## <a name="use-the-commerce-pricing-engine-in-sales"></a><span data-ttu-id="f0475-110">استخدام محرك التسعير التجاري في Sales</span><span class="sxs-lookup"><span data-stu-id="f0475-110">Use the Commerce pricing engine in Sales</span></span>

> [!NOTE]
> <span data-ttu-id="f0475-111">حاليًا، يمكن استخدام محرك التسعير التجاري فقط لإنشاء عروض الأسعار في Sales.</span><span class="sxs-lookup"><span data-stu-id="f0475-111">Currently, the Commerce pricing engine can be used only for quotation creation in the Sales.</span></span> <span data-ttu-id="f0475-112">تكامل أمر المبيعات مع محرك التسعير التجاري غير متاح بعد.</span><span class="sxs-lookup"><span data-stu-id="f0475-112">Sales order integration with the Commerce pricing engine isn't yet available.</span></span>

<span data-ttu-id="f0475-113">عندما يبدأ المستخدمون عرض أسعار في Sales، ينسخ إطار عمل الكتابة المزدوجة تفاصيل عرض الأسعار إلى Commerce.</span><span class="sxs-lookup"><span data-stu-id="f0475-113">When users initiate a quotation in Sales, the dual-write framework copies the quotation details to Commerce.</span></span> <span data-ttu-id="f0475-114">يتم نسخ أي تغييرات على بنود عروض الأسعار الحالية أو أي بنود عروض أسعار مضافة حديثًا في Sales إلى Commerce.</span><span class="sxs-lookup"><span data-stu-id="f0475-114">Any changes to existing quotation lines or any newly added quotation lines in Sales are copied to Commerce.</span></span> <span data-ttu-id="f0475-115">عندما يرغب المستخدمون في استخدام محرك التسعير التجاري لتسعير عرض الأسعار، يمكنهم تحديد **عرض أسعار السعر** لتحديث أسعار عرض الأسعار، بناءً على محرك التسعير التجاري.</span><span class="sxs-lookup"><span data-stu-id="f0475-115">When users want to use the Commerce pricing engine to price the quotation, they can select **Price quote** to update the prices of the quotation, based on the Commerce pricing engine.</span></span> <span data-ttu-id="f0475-116">يتم تحديث الأسعار تلقائيًا في كل من Sales وCommerce.</span><span class="sxs-lookup"><span data-stu-id="f0475-116">Prices are then automatically updated in both Sales and Commerce.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f0475-117">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="f0475-117">Prerequisites</span></span>

- <span data-ttu-id="f0475-118">قبل أن تتمكن من استخدام محرك تسعير Commerce في Sales، يجب عليك اتباع الخطوات الواردة في [العميل المتوقع إلى النقدية في الكتابة المزدوجة](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).</span><span class="sxs-lookup"><span data-stu-id="f0475-118">Before you can use the Commerce pricing engine in Sales, you must follow the steps in [Prospect-to-cash in dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).</span></span>
- <span data-ttu-id="f0475-119">يجب عليك إيقاف تشغيل تقييم الاتفاقية التجارية للإدخال اليدوي باتباع الخطوات التالية:</span><span class="sxs-lookup"><span data-stu-id="f0475-119">You must turn off trade agreement evaluation for manual entry by following these steps:</span></span>

    1. <span data-ttu-id="f0475-120">في بيئة Commerce، انتقل إلى **الحسابات المدينة\> إعداد \>معلمات الحسابات المدينة**.</span><span class="sxs-lookup"><span data-stu-id="f0475-120">In your Commerce environment, go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    1. <span data-ttu-id="f0475-121">في علامة التبويب **الأسعار**، في علامة التبويب السريع **سياسات تقييم الاتفاقية التجارية**، قم بإلغاء تحديد خانة الاختيار **الإدخال اليدوي**.</span><span class="sxs-lookup"><span data-stu-id="f0475-121">On the **Prices** tab, on the **Trade agreement evaluation** FastTab, clear the **Manual entry** check box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f0475-122">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="f0475-122">Additional resources</span></span>

[<span data-ttu-id="f0475-123">العميل المتوقع إلى النقدية في الكتابة المزدوجة</span><span class="sxs-lookup"><span data-stu-id="f0475-123">Prospect-to-cash in dual-write</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)
