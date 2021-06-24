---
title: الرقم التسلسلي للإرجاع-المنتجات المتحكمة في نقطة البيع
description: يصف هذا الموضوع قدرات التحقق من صحة الأصناف المتسلسلة كجزء من عملية الإرجاع في تطبيق نقطة البيع (POS) Microsoft Dynamics 365 Commerce.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7a067994828f3df577c0dc4146d26ac81990d4ac
ms.sourcegitcommit: 927574c77f4883d906e5c7bddf0af9b717e492bf
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129791"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a><span data-ttu-id="6b44b-103">الرقم التسلسلي للإرجاع–المنتجات المتحكمة في نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="6b44b-103">Return serial number–controlled products in POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="6b44b-104">يصف هذا الموضوع قدرات التحقق من صحة الأصناف المتسلسلة كجزء من عملية الإرجاع في تطبيق نقطة البيع (POS) Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6b44b-104">This topic describes the capabilities for validating serialized items as part of the return process in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

> [!NOTE]
> <span data-ttu-id="6b44b-105">في Commerce الإصدار 10.0.20 والإصدارات الأحدث، تتوفر ميزة جديدة تسمى **تجربة معالجة الإرجاع الموحدة في نقطة البيع**.</span><span class="sxs-lookup"><span data-stu-id="6b44b-105">In the Commerce version 10.0.20 release and later, a new feature that is named **Unified return processing experience in POS** is available.</span></span> <span data-ttu-id="6b44b-106">لاستخدام التحقق من صحة الرقم المسلسل أثناء معالجة أمر الإرجاع في نقطة البيع، يجب تشغيل هذه الميزة.</span><span class="sxs-lookup"><span data-stu-id="6b44b-106">To use serial number validation during return order processing in POS, you must turn on this feature.</span></span> <span data-ttu-id="6b44b-107">للحصول على معلومات حول القدرات الأخرى التي تقدمها هذه الميزة عند تشغيلها، راجع [(إنشاء مرتجعات في نقطة البيع)](POS-returns.md).</span><span class="sxs-lookup"><span data-stu-id="6b44b-107">For information about others capabilities that this feature provides when it's turned on, see [Create returns in POS)](POS-returns.md).</span></span>
>
> <span data-ttu-id="6b44b-108">بعد تشغيل الميزة، يتعذر إيقاف تشغيلها.</span><span class="sxs-lookup"><span data-stu-id="6b44b-108">After the feature is turned on, it can't be turned off.</span></span>

## <a name="options-for-validating-serialized-returns"></a><span data-ttu-id="6b44b-109">خيارات للتحقق من صحة المرتجعات المتسلسلة</span><span class="sxs-lookup"><span data-stu-id="6b44b-109">Options for validating serialized returns</span></span>

<span data-ttu-id="6b44b-110">عند تشغيل الميزة **تجربة معالجة الإرجاع الموحدة في نقطة البيع**، يمكن للمؤسسات إجراء التحقق من الصحة لمرتجعات الرقم التسلسلي–العناصر المتحكم فيها من خلال نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="6b44b-110">When the **Unified return processing experience in POS** feature is turned on, organizations can perform a validation on returns of serial number–controlled items through POS.</span></span> <span data-ttu-id="6b44b-111">يمكن أن تحذر هذه القدرة المستخدمين إذا كان الرقم التسلسلي الذي يتم إرجاعه يختلف عن الرقم التسلسلي الأصلي الذي تم بيعه.</span><span class="sxs-lookup"><span data-stu-id="6b44b-111">This capability can warn users if the serial number that is being returned differs from the original serial number that was sold.</span></span> <span data-ttu-id="6b44b-112">في Commerce، الإصدار 10.0.20 والإصدرات الأحدث، تكون الرسالة التي يتلقاها المستخدمون عبارة عن رسالة تحذير فقط.</span><span class="sxs-lookup"><span data-stu-id="6b44b-112">In the Commerce version 10.0.20 release and later, the message that users receive is only a warning message.</span></span> <span data-ttu-id="6b44b-113">يمكن للمستخدمين الاستمرار في معالجة إرجاع مقابل رقم تسلسلي يختلف عن الرقم التسلسلي الذي تم بيعه في الأصل.</span><span class="sxs-lookup"><span data-stu-id="6b44b-113">Users can continue to process a return against a serial number that differs from the serial number that was originally sold.</span></span>

<span data-ttu-id="6b44b-114">لتكوين التحقق من صحة الرقم التسلسلي لمؤسسة ما بعد تشغيل الميزة **تجربة معالجة الإرجاع الموحدة في نقطة البيع**، انتقل إلى **البيع بالتجزئة وCommerce \> إعداد المركز الرئيسي \> معلمات \> معلمات Commerce** في مركز Commerce الرئيسي.</span><span class="sxs-lookup"><span data-stu-id="6b44b-114">To configure serial number validation for an organization after the **Unified return processing experience in POS** feature is turned on, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters** in Commerce headquarters.</span></span> <span data-ttu-id="6b44b-115">في علامة التبويب **المخزون**، في علامة التبويب السريعة **عمليات مخزن المتجر**، قم بتعيين الخيار **تمكين التحقق من صحة الأرقام التسلسلية على مرتجعات نقطة البيع** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="6b44b-115">On the **Inventory** tab, on the **Store inventory operations** FastTab, set the **Enable validation of serial numbers on POS returns** option to **Yes**.</span></span>

## <a name="process-returns-for-serialized-items-in-pos"></a><span data-ttu-id="6b44b-116">معالجة المرتجعات للأصناف المتسلسلة في نقطة البيع</span><span class="sxs-lookup"><span data-stu-id="6b44b-116">Process returns for serialized items in POS</span></span>

<span data-ttu-id="6b44b-117">إذا تم تعيين الخيار **تمكين التحقق من صحة الأرقام التسلسلية في مرتجعات نقطة البيع** إلى **نعم**، عند إرجاع الرقم التسلسلي للصنف الذي يتم التحكم فيه من خلال نقطة البيع، يمكن للمستخدم إدخال الرقم التسلسلي لبند الإرجاع في جزء التفاصيل الموجود في الصفحة **المنتجات القابلة للإرجاع**.</span><span class="sxs-lookup"><span data-stu-id="6b44b-117">If the **Enable validation of serial numbers on POS returns** option has been set to **Yes**, when a serial number–controlled item is returned through POS, the user can enter the serial number for the return line in the details pane on the **Returnable products** page.</span></span> <span data-ttu-id="6b44b-118">إذا لم يتطابق الرقم التسلسلي الذي يتم إدخاله مع الرقم التسلسلي الأصلي الذي تم بيعه لحركة المبيعات، سيتلقى المستخدم رسالة تحذير.</span><span class="sxs-lookup"><span data-stu-id="6b44b-118">If the serial number that is entered doesn't match the original serial number that was sold for the sales transaction, the user receives a warning message.</span></span> <span data-ttu-id="6b44b-119">ومع ذلك، لا يمنع التطبيق المستخدم من متابعة ترحيل الإرجاع.</span><span class="sxs-lookup"><span data-stu-id="6b44b-119">However, the application doesn't prevent the user from continuing to post the return.</span></span>

> [!NOTE]
> <span data-ttu-id="6b44b-120">حاليًا، تدعم نقطة البيع التحقق من صحة الأرقام التسلسلية في بنود الإرجاع فقط حيث لا تكون الكمية الأصلية المطلوبة أكثر من واحد.</span><span class="sxs-lookup"><span data-stu-id="6b44b-120">Currently, POS supports validation of serial numbers only on return lines where the original ordered quantity is no more than one.</span></span> <span data-ttu-id="6b44b-121">إذا كان قد تم إنشاء بند أمر المبيعات الأصلي في قناة بخلاف نقطة البيع، وإذا كانت الكمية التي تم طلبها للصنف المسلسل في بند المبيعات المحدد أكثر من واحد، فإنه لا يمكن إرجاع الصنف بشكل صحيح من خلال نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="6b44b-121">If the original sales order line was created in a non-POS channel, and if the quantity that was ordered for the serialized item on a given sales line is more than one, the item can't be correctly returned through POS.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6b44b-122">الموارد الإضافية</span><span class="sxs-lookup"><span data-stu-id="6b44b-122">Additional resources</span></span>

[<span data-ttu-id="6b44b-123">إنشاء مرتجعات في نقطة البيع.</span><span class="sxs-lookup"><span data-stu-id="6b44b-123">Create returns in POS</span></span>](POS-returns.md)
