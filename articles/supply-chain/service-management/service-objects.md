---
title: نظرة عامة على كائنات الخدمة
description: كائنات الخدمة هي منتجات العميل وأصوله التي يمكن تنفيذ خدمة لها.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29d2cf6a496fed8d9932d5c6d49f4560d7eabbbb
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979102"
---
# <a name="service-objects-overview"></a><span data-ttu-id="3a15d-103">نظرة عامة على كائنات الخدمة</span><span class="sxs-lookup"><span data-stu-id="3a15d-103">Service objects overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a15d-104">كائنات الخدمة هي منتجات العميل وأصوله التي يمكن تنفيذ خدمة لها.</span><span class="sxs-lookup"><span data-stu-id="3a15d-104">Service objects are a customer’s assets and products for which you can perform a service.</span></span> <span data-ttu-id="3a15d-105">ووفقًا لنوع الخدمة المقدمة، يمكن أن تكون الكائنات مادية أو معنوية:</span><span class="sxs-lookup"><span data-stu-id="3a15d-105">Depending on the type of service you provide, objects can be tangible or intangible:</span></span>

-  <span data-ttu-id="3a15d-106">الكائنات المادية هي عبارة عن أشياء مثل الآلة أو المبنى، والتي يمكن إجراء مهمة خدمة فعلية عليها.</span><span class="sxs-lookup"><span data-stu-id="3a15d-106">Tangible objects are things, such as a machine or a building, on which you can perform a physical service task.</span></span>

    <span data-ttu-id="3a15d-107">ويمكن أيضًا أن يكون كائن الخدمة المادية صنف مخزون تقوم بإنشائه في نموذج تفاصيل المنتجات الصادرة‬.</span><span class="sxs-lookup"><span data-stu-id="3a15d-107">A tangible service object can also be an inventory item that you create in the Released product details form.</span></span> <span data-ttu-id="3a15d-108">ووفقًا لمجموعة أبعاد المخزون التي تقوم بإرفاقها بالصنف، يمكنك إنشاء كائن الخدمة بمستوى تفاصيل يتضمن الرقم المسلسل للصنف.</span><span class="sxs-lookup"><span data-stu-id="3a15d-108">Depending on the inventory dimension group that you attach to the item, you can create a service object to a level of detail that includes the item serial number.</span></span> <span data-ttu-id="3a15d-109">ويمكن الاستفادة من ذلك عند ضرورة تتبع الصنف عينه الذي تمثله خدمة الكائن.</span><span class="sxs-lookup"><span data-stu-id="3a15d-109">This is useful when you must keep track of the exact item that the service object represents.</span></span>

    <span data-ttu-id="3a15d-110">ويمكن أيضًا أن يكون كائن الخدمة المادي صنفًا غير مرتبط مباشرة بالإنتاج المباشر للشركة أو سلسلة التوريد.</span><span class="sxs-lookup"><span data-stu-id="3a15d-110">A tangible service object can also be an item that is not directly related to a company's direct production or supply chain.</span></span> <span data-ttu-id="3a15d-111">على سبيل المثال، يمكن أن تكون مجموعة الأدوات المستخدمة للإصلاحات في أمر خدمة عبارة عن كائن خدمة غير مضمن في المخزون.</span><span class="sxs-lookup"><span data-stu-id="3a15d-111">For example, a tool kit that is used for repairs in a service order can be a service object that is not included in inventory.</span></span> <span data-ttu-id="3a15d-112">في هذه الحالة، يمكنك عدم تسجيلها كصنف مخزون.</span><span class="sxs-lookup"><span data-stu-id="3a15d-112">In this case, you don’t register it as an inventory item.</span></span>

-  <span data-ttu-id="3a15d-113">الكائنات المعنوية عبارة عن أشياء غير مادية مثل مجموعة حسابات أو مستندات قانونية، يتم إجراء مهام الخدمة عليها.</span><span class="sxs-lookup"><span data-stu-id="3a15d-113">Intangible objects are nonphysical things, such as a set of accounts or a legal document, on which you can perform a service task.</span></span>

## <a name="example-of-an-intangible-service-object"></a><span data-ttu-id="3a15d-114">مثال على كائن الخدمة غير المادي</span><span class="sxs-lookup"><span data-stu-id="3a15d-114">Example of an intangible service object</span></span>

<span data-ttu-id="3a15d-115">تحتفظ الشركة "أ" بالسجلات المالية للعديد من الشركات الصغيرة.</span><span class="sxs-lookup"><span data-stu-id="3a15d-115">Company A maintains the financial records for several small companies.</span></span> <span data-ttu-id="3a15d-116">وأحد عملاء الشركة "أ" هو فريق الكرة المحلي، وتقوم الشركة "أ" بأعمال مسك الدفاتر الأسبوعية والمراجعة السنوية لهذا الفريق.</span><span class="sxs-lookup"><span data-stu-id="3a15d-116">One of Company A's clients is the local football team, for which Company A does the weekly bookkeeping and annual audit of the club's accounts.</span></span> <span data-ttu-id="3a15d-117">ويتم إعداد حسابات الفريق في نموذج كائنات الخدمة ويتم تعيينها ككائن في اتفاقية الخدمة.</span><span class="sxs-lookup"><span data-stu-id="3a15d-117">The club's accounts are set up in the Service objects form and specified as the object in the service agreement.</span></span> <span data-ttu-id="3a15d-118">يوجد اثنان من بنود اتفاقية الخدمة للكائن.</span><span class="sxs-lookup"><span data-stu-id="3a15d-118">There are two service agreement lines for the object.</span></span> <span data-ttu-id="3a15d-119">البند 1 هو أعمال مسك الدفاتر الأسبوعية بفترات أسبوعية معينة للبند، والبند 2 هو المراجعة السنوية بفترة سنوية معينة لها.</span><span class="sxs-lookup"><span data-stu-id="3a15d-119">Line 1 is weekly bookkeeping with a weekly interval assigned to the line, and line 2 is the annual audit with a yearly interval assigned to it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a15d-120">مواضيع مرتبطة</span><span class="sxs-lookup"><span data-stu-id="3a15d-120">Related topics</span></span>

[<span data-ttu-id="3a15d-121">إنشاء كائنات خدمة</span><span class="sxs-lookup"><span data-stu-id="3a15d-121">Create service objects</span></span>](create-service-objects.md)

